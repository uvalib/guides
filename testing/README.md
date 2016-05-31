# Testing Recommendations

https://www.polymer-project.org/1.0/docs/tools/tests

## Unit Testing

### Web Component Tester (WCT)

This testing tool can be run locally on the development environment and on the Travis CI site.

### Selenium


## Travis

Travis provides an Ubuntu testing platform. The sample file included here is configured for the 64-bit Ubuntu 14.02 version which is necessary for running tests against Chrome. To test other platforms, we include SauceLabs connectivity. The configuration file included here contains most of the settings required for our testing. Additional configuration information for integrating with SauceLabs is documented in the next section. 

Follow the directions to [connecting your GitHub account with Travis](https://github.com/Polymer/tools/tree/master/travis).

After you have started using Travis to test builds, you may update your GitHub project readme file to include the Travis build status by clicking on the status icon in Travis. Then copy the appropriate markup syntax and paste it into your GitHub readme.

## SauceLabs

We use this testing environment to test across multiple operating systems and devices which we know our patrons are using. Make sure you follow the [directions for integrating Sauce with WCT](https://github.com/Polymer/tools/tree/master/travis#wct-with-sauce). The access key required for this is found in the SauceLabs account under the settings. The secure keys added to the Travis YAML file are repository specific. So don't try to copy a Travis config file from one repo to another.
