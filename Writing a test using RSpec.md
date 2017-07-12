# Writing a test using RSpec (Project Euler)

* In terminal ``` respec --init``` to intialise project with rspec creates spechelper.rb
Will create .rspec initialiser file.
spec_helper.rb file, where we can write our configuration.



* Require rspec ``` require 'rspec'```
* Configure the file 


``` 
RSpec.configure do |config|

end 

```

* Describe what the test should do 

```
describe "Description" do 
end
```

*


```
require 'httparty'
include HTTParty



response = HTTParty.get('http://bbc.co.uk/news')
puts response.body # prints body of html response
puts response.message # prints message of code (ok)
puts response.code # prints code received (200)

puts response.header.inspect # print header of html response
```