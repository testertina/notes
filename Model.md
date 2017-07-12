# Models

File: Week 5, day 3 sinatra models.

Singular, has a class which contains methods that interact with databases.

ie. 
```
class post
end
```
	
```
	def self.open_connection
		conn = PG.connect( dbname: "blog")
	end
```

self is a Class method.

Called by ``` Post.open_connection ```