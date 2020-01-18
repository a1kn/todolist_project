require "bundler/gem_tasks"
require 'rake/testtask'
require 'find'

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'List files'
task :list do
  Find.find('.') do |name|
    next if name.include?('/.')
    puts name if File.file?(name)
  end
end
