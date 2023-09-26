require "rake/testtask"
require 'find'

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'list every file in project (except those tht start with . and those that reside in directory whose name begins with ..'
task :files do 
	Find.find('.') do |file|
		next if file.include?("/.")
		puts file if File.file?(file)
	end
end