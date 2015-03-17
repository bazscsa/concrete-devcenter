---
title: Bitrise Appium Test Step
---

# Bitrise Appium Test Step

To run your [Appium](http://appium.io/) tests during a build on Bitrise you only have to follow these three easy steps:

* Add the Appium test step to your workflow. 
* Name your main test script appium-test.rb and place it in the Tests folder (/Tests/appium-test.rb). You can run other steps from this script.
* Make your script ready to receive the application folder as a parameter

(You can use this code snippet):
    

    require 'optparse'
    require 'yaml'

    options = {}
    OptionParser.new do |opts|
      opts.banner = "Usage: example.rb [options]"

      opts.on('-f', '--appfolder APPFOLDER', 'Application folder') { |v| options[:appfolder] = v }

    end.parse!

    APP_PATH = options[:appfolder]
    desired_caps = {
      caps:       {
        platformName:  'iOS',
        versionNumber: '7.1',
        deviceName:    'iPhone Simulator',
        app:           APP_PATH,	
      },
      appium_lib: {
        sauce_username:   nil, # don't run on Sauce
        sauce_access_key: nil
      }
    }

    # Start the driver
    Appium::Driver.new(desired_caps).start_driver

    # ... insert your code

    #driver_quit


And that's it. The step starts the appium server and uses [Bundler](http://bundler.io/] to run your ruby appium step. You can also create screenshots during the test just keep in mind to save the screenshots to the Tests/Screenshots folder.