# This must! be run with ruby1.8!
# Unless you enabled RUBYOPTS ENV in Gemfile.
require 'rake'
require 'rubygems'
require 'puppetlabs_spec_helper/rake_tasks'
require 'puppet-lint'
require 'rspec/core/rake_task'
require 'puppet-lint/tasks/puppet-lint'

desc 'Run the tests'
RSpec::Core::RakeTask.new(:do_test) do |t|
  t.rspec_opts = ['--color', '-f d']
  t.pattern = 'spec/*/*_spec.rb'
end

desc 'Run the test without refreshing fixtures'
RSpec::Core::RakeTask.new(:do_local) do |t|
    t.rspec_opts = ['-c', '-f d']
    # do only defines
    t.pattern = 'spec/defines/*_spec.rb'
end

PuppetLint::RakeTask.new(:lint) do |config|
  # Pattern of files to check, defaults to `**/*.pp`
  config.pattern = 'manifests/**/*.pp'

  # Pattern of files to ignore
  #config.ignore_paths = ['vendor/**/*.pp']

  # List of checks to disable
  config.disable_checks = ['80chars', 'documentation', 'autoloader_layout', 'class_inherits_from_params_class']

  # Should the task fail if there were any warnings, defaults to false
  #config.fail_on_warnings = true

  # Print out the context for the problem, defaults to false
  # config.with_context = true
end

task :default => [:spec_prep, :do_test]
task :local => [:spec_prep, :do_local]
task :test => [:default]
task :clean => [:spec_clean]
