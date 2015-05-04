namespace :site do
  desc "Build and preview the site in your browser"
  task :preview do
    require "launchy"

    # Wait a few seconds for the site to generate, then open it in a browser.
    Thread.new do
      sleep 4
      Launchy.open("http://localhost:4000")
    end

    # Build the site, watch for changes, and serve on localhost.
    system "bundle exec jekyll serve --watch"
  end

  desc "Build the site"
  task :build do
    system "bundle exec jekyll build"
  end
end

namespace :post do
  desc "Create new post"
  task :new, :title do |_, args|
    require 'active_support/core_ext/string/inflections'

    abort "Please specify a title\nrake post:new[Hello World]" unless args.title

    today = Time.new.strftime('%Y-%m-%d')
    filename = "_posts/#{today}-#{args.title.parameterize}.md"

    File.open(filename, "wb") do |post|
      post.puts("---")
      post.puts("layout: post")
      post.puts(%Q[title: "#{args.title.titlecase}"])
      post.puts("quote: false")  # Appears below the title.
      post.puts("date: #{Time.new.strftime('%Y-%m-%d %H:%M')}")  # Overrides the date from the name of the post. Useful for sorting posts.
      post.puts("author: Dennis Ideler")
      post.puts("categories: []")
      post.puts("image: false")  # E.g. /media/2014-01-30-hello/cover.jpg or http://example.com/hi.png
      post.puts("comments: false")  # Comments powered by Disqus.
      post.puts("---")
      post.puts
      post.puts
    end

    puts "Created #{filename}"
  end
end
# TODO: livereload
