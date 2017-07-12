# Selenium

Server which talks to a browser (Google Chrome, Firefox Gecko, IE driver). Software testing framework for web applications.

Download Selenium Chrome driver for mac64 and Selenium Gecko driver for mac.

Selenium cheat sheet 

* https://gist.github.com/huangzhichong/3284966

* http://www.rubydoc.info/gems/selenium-webdriver/Selenium/WebDriver/Chrome

```
require 'selenium-webdriver'

# Module Selenium and going to the class WebDriver, created an object in the file.
# Chrome driver quits automatically
driver = Selenium::WebDriver.for :chrome

# Chrome loads google.co.uk
driver.get 'http://www.google.co.uk'

# Inspect the search bar element and find its name.
search_bar = driver.find_element :name => "q"

```


# Watir

http://watir.github.io/docs/elements/

http://www.rubydoc.info/gems/watir-webdriver


# Testing advice

* Make a user journey (i.e. I can log into bbc.co.uk)

* Each user journey has scenarios

GIVEN - The sign page loads

WHEN - I input correct login details

AND - click submit

THEN - My specific homepage will load

