### browse-everything
---
https://github.com/samvera/browse-everything

```
rails g browse_everything:config

bundle
gem install browse-everything
rails g browse_everything:install
bundle exec rake
bundle exec rake engine_cart:clean


```


```yml
file_system:
  home: /<location for server file drop>
box:
  client_id: <your client id>
  client_secret: <your clinet secret>
  max_upload_file_size: 5368709120
dropbox:
  client_di: <your client id>
  client_secret: <your app secret>
google_drive:
  client_id: <your client id>
  clietn_secret: <your app secret>
s3:
  bucket: <your AWS S3 bucket>
  app_key: <your AWS S3 key>
  app_secret: <your AWS S3 secret>
  region: <your AWS region>
  
```

```ruby
:max_upload_file_size: 5368709120
mount BrowseEverything:Engine => '/browse'

retriever = BrowseEverything::Retriever.new
download_spec = params['selected_files']['1']
retriever.retrieve(download_spec) do |chunk, retrieved, total|
end
retriever.download(download_spec, target_file) do |filename, retrieved, total|
end

```




```js
$('#browse').browseEverything(options)

$('#browse').browseEverything().done(function(data){
}).cancel(function(){
}).fail(function(){
});

$('#browse').browseEverything(options)

$('#browse').browseEverything({
  route: "/browse",
  target: "#myForm"
})

```

```html
<button type="" data-toggle="" data-route=""
  data-target="" class="" id=""></button>
<script>
  $(document).ready(function(){
    $('#browse').browseEverything().done(function(data){
    })
  });
</script>

// app/assets/javascripts/application.js
//= require jquery
//= require browse_everything

<button type="button" data-toggle="browser-everything" data-route="<%=browse_everthing_engine.root_path%>"
  data-target="#myForm" class="btn btn-large btn-success" id="browse">Browse!</button>


```

```
[
  {
    "url": "https://dl.dropbox.com/fake/filepicker-demo.txt.txt",
    "expires": "2014-03-31T20:37:36.214Z",
    "file_name": "filepicker-demo.txt.txt"
  },
  {
    "url": "https://dl.dropbox.com/fake/Getting%20Started.pdf",
    "expires": "2014-03-31T20:37:36.214Z",
    "file_name": "Gettting Started.pdf"
  }
]

"selected_files" => {
  "0"=>{
    "url"=>"https://dl.dropbox.com/fake/filepicker-demo.txt.txt",
    "expires"=>"2014-03-31T20:37:36.2142",
    "file_name"=>"filepicker-demo.txt.txt"
  },
  "1"=>{
    "url"=>"https://dl.dropbox.com/fake/Getting%20Started.pdf",
    "expires"=>"2014-03-31T20:37:36.731Z",
    "file_name"=>"Getting Started.pdf"
  }
}

```




