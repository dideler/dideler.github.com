# Based off of Jekyll's Rakefile

namespace :site do
  desc "Generate and view the site locally"
  task :preview do
    require "launchy"

    # Yep, it's a hack! Wait a few seconds for the Jekyll site to generate and
    # then open it in a browser. Someday we can do better than this, I hope.
    Thread.new do
      sleep 4
      puts "Opening in browser..."
      Launchy.open("http://localhost:4000")
    end

    # Generate the site in server mode.
    puts "Running Jekyll..."
    system "bundle exec jekyll serve --watch"
  end

  namespace :releases do
    desc "Create new release post"
    task :new, :version do |t, args|
      raise "Specify a version: rake site:releases:new['1.2.3']" unless args.version
      today = Time.new.strftime('%Y-%m-%d')
      release = args.version.to_s
      filename = "site/_posts/#{today}-jekyll-#{release.split('.').join('-')}-released.markdown"

      File.open(filename, "wb") do |post|
        post.puts("---")
        post.puts("layout: news_item")
        post.puts("title: 'Jekyll #{release} Released'")
        post.puts("date: #{Time.new.strftime('%Y-%m-%d %H:%M:%S %z')}")
        post.puts("author: ")
        post.puts("version: #{release}")
        post.puts("categories: [release]")
        post.puts("---")
        post.puts
        post.puts
      end

      puts "Created #{filename}"
    end
  end
end

#############################################################################
#
# Packaging tasks
#
#############################################################################

task :release => :build do
  unless `git branch` =~ /^\* master$/
    puts "You must be on the master branch to release!"
    exit!
  end
  system "git commit --allow-empty -m 'Release #{version}'"
  system "git tag v#{version}"
  system "git push origin master"
  system "git push origin v#{version}"
end
