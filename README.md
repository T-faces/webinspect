# webinspect
Ruby gem to inspect completely a web page. It scrapes a given URL, and returns you its meta, links, images more.

# See it in action!
You can try WebInspector live at this little demo: https://scrappet.herokuapp.com

# Installation
Add this line to your application's Gemfile:

gem 'webinspector'
And then execute:

$ bundle
Or install it yourself as:

$ gem install webinspector
Usage
Initialize a WebInspector instance for an URL, like this:

page = WebInspector.new('http://davidesantangelo.com')
Accessing response status and headers
You can check the status and headers from the response like this:

page.response.status  # 200
page.response.headers # { "server"=>"apache", "content-type"=>"text/html; charset=utf-8", "cache-control"=>"must-revalidate, private, max-age=0", ... }
Accessing inpsected data
You can see the data like this:

page.url                 # URL of the page
page.scheme              # Scheme of the page (http, https)
page.host                # Hostname of the page (like, davidesantangelo.com, without the scheme)
page.port                # Port of the page
page.title               # title of the page from the head section, as string
page.description         # description of the page
page.links               # every link found
page.images              # every image found
page.meta                # metatags of the page
Accessing meta tags
page.meta                 # metatags of the page
page.meta['description']  # meta description
page.meta['keywords']     # meta keywords
Find words (as array)
page.find(["word1, word2"]) # return {"word1"=>3, "word2"=>1}
Contributors
Steven Shelby (@stevenshelby)
Sam Nissen (@samnissen)
License
The webinspector GEM is released under the MIT License.

# Contributing
Fork it ( https://github.com/[my-github-username]/webinspector/fork )
Create your feature branch (git checkout -b my-new-feature)
Commit your changes (git commit -am 'Add some feature')
Push to the branch (git push origin my-new-feature)
Create a new Pull Request

credit by : @davidesantangelo
