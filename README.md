# Rails Semantic Logger
[![Gem Version](https://img.shields.io/gem/v/rails_semantic_logger.svg)](https://rubygems.org/gems/rails_semantic_logger) [![Build Status](https://github.com/reidmorrison/rails_semantic_logger/workflows/build/badge.svg)](https://github.com/reidmorrison/rails_semantic_logger/actions?query=workflow%3Abuild) [![Downloads](https://img.shields.io/gem/dt/rails_semantic_logger.svg)](https://rubygems.org/gems/rails_semantic_logger) [![License](https://img.shields.io/badge/license-Apache%202.0-brightgreen.svg)](http://opensource.org/licenses/Apache-2.0) ![](https://img.shields.io/badge/status-Production%20Ready-blue.svg)

Rails Semantic Logger replaces the Rails default logger with [Semantic Logger](https://logger.rocketjob.io/)

* http://github.com/reidmorrison/rails_semantic_logger

## Fork Details

This fork of Rails Semantic Logger extends the functionality of the original gem by adding the response object to the payload returned by the `process_action` method in `lib/rails_semantic_logger/action_controller/log_subscriber.rb`. This enhancement allows users to access information about the response in their logging.

### Added Features

- Includes the response object in the payload returned by the `process_action` method.

### Usage

To use this fork in your Rails application, simply include it in your Gemfile:

```ruby
gem 'rails_semantic_logger', git: 'https://github.com/firstpromoter/rails_semantic_logger.git'
```

## Documentation

For complete documentation see: https://logger.rocketjob.io/rails

## Upgrading to Semantic Logger v4.4

With some forking frameworks it is necessary to call `reopen` after the fork. With v4.4 the
workaround for Ruby 2.5 crashes is no longer needed. 
I.e. Please remove the following line if being called anywhere:

~~~ruby
SemanticLogger::Processor.instance.instance_variable_set(:@queue, Queue.new)
~~~

## Supports

For the complete list of supported Ruby and Rails versions, see the [Testing file](https://github.com/reidmorrison/rails_semantic_logger/blob/master/.github/workflows/ci.yml).

## Author

[Reid Morrison](https://github.com/reidmorrison)

[Contributors](https://github.com/reidmorrison/rails_semantic_logger/graphs/contributors)

## Versioning

This project uses [Semantic Versioning](http://semver.org/).

