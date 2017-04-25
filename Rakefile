require 'bundler/gem_tasks'
require 'rspec/core/rake_task'
require 'rake/clean'
require 'rake/extensiontask'

RSpec::Core::RakeTask.new(:spec)

task default: :spec
task spec: :compile

CLEAN.include('ext/**/Makefile', 'ext/**/*.{o,so}', 'lib/**/*.{o,so}')

Rake::ExtensionTask.new 'agrian_gdal' do |ext|
  ext.lib_dir = 'lib'
end
