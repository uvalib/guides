# Testing Recommendations


## Unit Testing

Unit tests should be developed for expected results, as well as the unexpected. For example, if you don't expect null as a possible result then test to see if it can occur by creating multiple test fixtures with different values and make sure all asserts for not null pass.

### Web Component Tester (WCT)

[Testing documentation for Polymer](https://www.polymer-project.org/1.0/docs/tools/tests) identifies Mocha, Selenium, etc. used by WCT. This testing tool can be run locally on the development environment and on the Travis CI site.

After using the Yeoman process to create a new web component
`yo polymer:seed <component-name>`,
the component's README file will provide information on installation of this tool and how to execute it.

Configuration settings for WCT are stored in a wct.conf.json file. To run WCT on your development box and exclude SauceLabs testing, you need to add 
`      "disabled": true,` 
to the sauce section of the wct.conf.json file. But this needs to be removed when committing the changes and running tests via Travis; otherwise the SauceLabs testing will result in an error indicating no browser configuration was specified.

## Travis

Travis provides an Ubuntu testing platform. The sample file included here is configured for the 64-bit Ubuntu 14.02 version which is necessary for running tests against Chrome. To test other platforms, we include SauceLabs connectivity. The configuration file included here contains most of the settings required for our testing. Additional configuration information for integrating with SauceLabs is documented in the next section. 

Follow the directions to [connecting your GitHub account with Travis](https://github.com/Polymer/tools/tree/master/travis).

After you have started using Travis to test builds, you may update your GitHub project readme file to include the Travis build status by clicking on the status icon in Travis. Then copy the appropriate markup syntax and paste it into your GitHub readme.

## SauceLabs

We use this testing environment to test across multiple operating systems and devices which we know our patrons are using. Make sure you follow the [directions for integrating Sauce with WCT](https://github.com/Polymer/tools/tree/master/travis#wct-with-sauce). The access key required for this is found in the SauceLabs account under the settings. 

The secure keys added to the Travis YAML file are repository specific. So don't try to copy a Travis config file from one repo to another.

The various operating system and devices to be tested on SauceLabs should be configured in the WCT configuration file so that Travis can automate the process.
