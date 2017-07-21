# Appium

Test automation framework for use with native, hybrid and mobile web apps. Allows you to simulate browser interaction with OS framework. Uses selenium and capybara wrappers.

Supported platforms:

* iOS
* Wiley foxphones
* Android

Appium is a node/npm based language for ruby.

## Physical devices

Deploys an app (appium that is a selenium server) from your local machine onto a physical phone and this can be accessed locally using a PC.

## Virtual devices

SDK dedicates RAM and CPU for a singular instance of a virtual device, so a virtual device is hosted on your local machine.

Create a capabilities JSON to find the device name and emulator number.  When it connects it deploys a selenium server to it.

Software development kit SDK

## Android Studio
Allows us to create a virtual android device.

* Download all APKs needed for Android OS you are interested in.
* Follow through instructions to create a virtual device: Tools > Android > AVD kit.
* In advanced settings after creating a device you can changes things like webcam capability.

``` adb devices ``` shows which devices are being emulated.
``` adb install "file path" ``` will install android packet kit (apk) to virtual device.

## Using Appium

* Open appium
* Select start server
* Create a new automatic server
* Set JSON for local system properties

```
{
  "platformName": "Android",
  "platformVersion": "7.1.1",
  "deviceName": "emulator-5554",
  "app": "/Users/kierancornwall/Downloads/ContactManager.apk"
}
```

Where app is the apk you want to use. The platformVersion matches the version you are simulating.

* Click start session (This makes appium connect to the virtual device.
* Can select Divs, Buttons, etc to find their id.


## RSpec with Appium

* Create rspec files with ``` rspec --init ```
* Set up environment in spec_helper. Define Appium driver using def

```
require 'rspec'
require 'pry'
require 'appium_lib'

RSpec.configure do|config|
  config.color = true
  config.tty = true
  config.formatter = :documentation
end

def desired_capabilities
     { caps: {
          platformName: "Android",
          deviceName: "emulator-5554",
          app: "/Users/kierancornwall/Downloads/ContactManager.apk",
      }
     }
end
```

* Create a appium spec file to initiate an instance of a driver.

```
require 'spec_helper'

describe 'Testing stuff' do

	# Starts the appium driver defined in spec helper.
	before(:all) do
		Appium::Driver.new(desired_capabilities).start_driver
		# Module level method that allows you to pass a class which will inherit all of the appium methods.
		Appium.promote_appium_methods(RSpec::Core::ExampleGroup)
	end

	# Closes the appium driver at the end of all tests.
	after(:all) do
		driver.quit
	end

	it 'test stuff' do
		binding.pry
	end
	
end
```

* Run rspec in corresponding folder.  This will create a connection from the Appium server to the virtual device created in Android studio.
* You will open a connection in terminal which allow you to grab elements and test them from the virtual device by using id's found in Appium inspect.

``` find_element(:id, 'com.example.android.contactmanager:id/addContactButton').click ```


### Common Appium methods (courtesy of Kieran)

```
screenshot(path)

find_element(attribute: value) - Finds an element with the attribute specified.

find_elements(attribute: value) - Finds all elements with the attribute specified.

page - Shows you the DOM of the current screen. A useful alternative to the Appium Inspector.
```

```
textfields - Returns all the text fields within the current screen.

textfields('text') - Returns all the text fields within the current screen whose text attribute is equal to 'text'.

first_textfield - Returns the first text field within the current screen.

last_textfield - Returns the last text field within the current screen.

textfield('text') - Returns a textfield whose text attribute is equal to 'text'.

first_textfield.type('text') - Types in the word 'text' in the first textfield within the current screen.
```

Buttons

```
buttons - Returns all the buttons within the current screen.

buttons('text') - Returns all the buttons within the current screen whose text attribute is equal to 'text'.

first_button - Returns the first button within the current screen.

last_button - Returns the last button within the current screen.

button('text') - Returns a button whose text attribute is equal to 'text'.

first_button.click - Types in the word 'text' in the first button within the current screen.

first_button.text - Returns the text attribute of the first button within the current screen.
```

In appium we can combine appium methods with selenium methods. i.e.
``` first_text.text ```
This will use appium method first text to find the first text element.  Then it will use the selenium .text method to display the text within it.