# Sinatra and Web servers

```
class PenguinsController < Sinatra::Base

  configure :development do
      register Sinatra::Reloader
  end

```

Penguins is the resource name.

## ERB: embedded Ruby (framework)

Different templates: Angular, React.
ERB is HTML with ruby defined ruby variables.
Creating a file would be ``` index.erb ```

```
  # sets root as the parent-directory of the current file
  set :root, File.join(File.dirname(__FILE__), '..')

  # sets the view directory correctly
  set :views, Proc.new { File.join(root, "views") } 
```

Sets the root directory and views directory.

### Index rest name

```
  get '/' do
    erb :"penguins/index"
  end
```

The filepath is "/", this request is getting the index.erb file.

### erb tags

```
<%= @title %>
```
or

```
{{ @title }}

```
Shows a variable in index.erb.

```
  get '/' do
    @title = "Mr Magorium's Penguin Emporium"
    erb :"penguins/index"
  end
```

Then define the variable in the index request.

### methods

```
  post '/' do
    post = {
      id: $posts.length,
      title: params[:title],
      body: params[:body]
    }

    $posts.push post
    erb, send_file, redirect
  end
```

Need to end a method with a response type instruction: redirect, erb, send_file.
