require 'rake'
require 'rake/testtask'
require 'rdoc/task'

desc 'Default: run unit tests.'
task :default => :test

desc 'Test the ruby_encoding_wrapper plugin.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.libs << 'test'
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

desc 'Generate documentation for the ruby_encoding_wrapper plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'RubyEncodingWrapper'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README')
  rdoc.rdoc_files.include('lib/**/*.rb')
end


# build gem with jeweler's help
require 'jeweler'
Jeweler::Tasks.new do |gem|
  gem.name = "ruby-encoding-wrapper"
  gem.description = "Simple wrapper for encoding.com API based on ruby."
  gem.email = "info@antonzaytsev.com"
  gem.homepage = "https://github.com/mikhailov/ruby-encoding-wrapper"
  gem.authors = ["Mikhailov Anatoly", "Tsech Edward", "Anton Zaytsev"]
  gem.summary = "Ruby wrapper for Encoding.com API"
  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new