require 'bundler'
Bundler.setup(:default, :development)

$LOAD_PATH.unshift 'lib'
require 'scout_scout/version'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  gem.version = ScoutScout::VERSION
  gem.name = "scout_scout"
  gem.summary = %Q{API wrapper for scout.com}
  gem.description = %Q{API wrapper for scout.com}
  gem.email = "jnewland@gmail.com"
  gem.homepage = "http://github.com/jnewland/scout_scout"
  gem.authors = ["Jesse Newland"]
  # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  # dependencies are handled in Gemfile
end
Jeweler::GemcutterTasks.new

require 'rake/rdoctask'
Rake::RDocTask.new do |rdoc|
  version = ScoutScout::VERSION

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "scout_scout #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

desc "Open an irb session preloaded with this library"
task :console do
  sh "irb -rubygems -I lib -r scout_scout.rb"
end

require "rake/testtask"
Rake::TestTask.new do |test|
  test.libs << "test"
  test.test_files = [ "test/*.rb" ]
  test.verbose = true
end

task :default => :test