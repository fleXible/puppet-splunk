# Install via
# bundle install --path vendor/gems
#
if RUBY_VERSION =~ /1.9/ # assuming you're running Ruby ~1.9
       Encoding.default_external = Encoding::ASCII
       Encoding.default_internal = Encoding::ASCII
       ENV['RUBYOPT'] = '-Kn'
end

source 'https://rubygems.org'

if RUBY_VERSION < '1.9.3'
  gem 'rake', '< 11'
  gem 'retriable', '< 2'
  gem 'addressable', '< 2.4'
  gem 'json_pure', '< 2'
else
  gem 'rake', :require => false
end

gem 'mocha'
gem 'hiera-file'
gem 'puppet',        ENV['PUPPET_VERSION'] || '= 3.1.1'
gem 'facter',        if ENV['PUPPET_VERSION'] then '> 2.0' else '= 1.6.18' end
gem 'puppet-lint',   :git => 'https://github.com/rodjek/puppet-lint.git'
gem 'puppet-syntax'
gem 'rspec',         '< 2.99'
gem 'rspec-puppet'
#gem 'rake',          '= 10.4.2'
gem 'puppetlabs_spec_helper'


# puppet lint plugins
# https://puppet.community/plugins/#puppet-lint
gem 'puppet-lint-appends-check',
    :git => 'https://github.com/voxpupuli/puppet-lint-appends-check.git',
    :require => false
gem 'puppet-lint-classes_and_types_beginning_with_digits-check',
    :git => 'https://github.com/voxpupuli/puppet-lint-classes_and_types_beginning_with_digits-check.git',
    :require => false
gem 'puppet-lint-empty_string-check',
    :git => 'https://github.com/voxpupuli/puppet-lint-empty_string-check.git',
    :require => false
gem 'puppet-lint-file_ensure-check',
    :git => 'https://github.com/voxpupuli/puppet-lint-file_ensure-check.git',
    :require => false
gem 'puppet-lint-leading_zero-check',
    :git => 'https://github.com/voxpupuli/puppet-lint-leading_zero-check.git',
    :require => false
#gem 'puppet-lint-numericvariable',
#    :git => 'https://github.com/fiddyspence/puppetlint-numericvariable.git',
#    :require => false
gem 'puppet-lint-resource_reference_syntax',
    :git => 'https://github.com/voxpupuli/puppet-lint-resource_reference_syntax.git',
    :require => false
gem 'puppet-lint-spaceship_operator_without_tag-check',
    :git => 'https://github.com/voxpupuli/puppet-lint-spaceship_operator_without_tag-check.git',
    :require => false
#gem 'puppet-lint-strict_indent-check',
#    :git => 'https://github.com/relud/puppet-lint-strict_indent-check.git',
#    :require => false
gem 'puppet-lint-trailing_comma-check',
    :git => 'https://github.com/voxpupuli/puppet-lint-trailing_comma-check.git',
    :require => false
gem 'puppet-lint-undef_in_function-check',
    :git => 'https://github.com/voxpupuli/puppet-lint-undef_in_function-check.git',
    :require => false
gem 'puppet-lint-unquoted_string-check',
    :git => 'https://github.com/voxpupuli/puppet-lint-unquoted_string-check.git',
    :require => false
gem 'puppet-lint-variable_contains_upcase',
    :git => 'https://github.com/fiddyspence/puppetlint-variablecase.git',
    :require => false
gem 'puppet-lint-version_comparison-check',
    :git => 'https://github.com/voxpupuli/puppet-lint-version_comparison-check.git',
    :require => false
