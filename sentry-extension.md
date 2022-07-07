require "sentry-ruby"

# the integrable module needs to be required separately
require "sentry/integrable" 

module Sentry
  # the module/class of the extension should be defined under the Sentry namespace
  module Rails 
    
    # extend the module
    extend Integrable 
    
    # use the register_integration method to register your extension to the SDK core
    register_integration name: "rails", version: Sentry::Rails::VERSION
  end
end
