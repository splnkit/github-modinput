# Github Modular Input

The Github Modular Input is a splunk modular input developed as an example in the [Splunk SDK for Javascript](https://github.com/splunk/splunk-sdk-javascript) and is bundled separately here with its dependencies for easy deployment to [Splunkbase](http://apps.splunk.com). It provides a "native" Splunk input method that collects commit data via the Github API to be consumed in Splunk for search, analysis and correlation with other data sets.

There is a very thorough blog post about how it is implemented at [blog.splunk.com](http://blogs.splunk.com/2014/09/17/new-support-for-authoring-modular-inputs-in-node-js/) as well as extensive documentation about its components which is referenced below.

## Getting the Code

Github Repository: [https://github.com/splnkit/github-modinput](https://github.com/splnkit/github-modinput)

Original code was forked from [https://github.com/splunk/splunk-sdk-javascript/](https://github.com/splunk/splunk-sdk-javascript/tree/develop/examples/modularinputs/github_commits)

On Splunkbase at: TBD

## Install

In general there are two methods for installing apps into Splunk:

1. Copy this whole `github-modinput` folder to `$SPLUNK_HOME/etc/apps`.
2. Restart Splunk

or

1. From the App dropdown menu in your Splunk interface, click on "Find More Apps"
2. Search for "Github Modular Input" and follow the instructions to install. 

## Adding an input

1. From Splunk Home, click the Settings menu. Under **Data**, click **Data inputs**, and find `Github Commits`, the input you just added. **Click Add new on that row**.
2. Click **Add new** and fill in:
    * `name` (whatever name you want to give this input)
    * `owner` (the owner of the Github repository, this is a Github username or org name)
    * `repository` (the name of the Github repository)
    * (optional) `token` if using a private repository and/or to avoid Github's API limits. To get a Github API token visit the [Github settings page](https://github.com/settings/tokens/new) and make sure the `repo` and `public_repo` scopes are selected.
3. Save your input, and navigate back to Splunk Home.
4. Do a search for `sourcetype=github_commits` and you should see some commits indexed, if your repository has a large number of commits indexing them may take a few moments.


## Documentation
 
There is loads of documentation for Splunk, modular inputs, and the Splunk Javascript SDK so please refer to the following links to learn what these tools are, how they work and how you can build your own!

* Splunk Documentation: [Splunk Docs](http://docs.splunk.com/Documentation/Splunk)
* Splunk Modular Inputs: [Modular Inputs](http://docs.splunk.com/Documentation/Splunk/6.2.1/AdvancedDev/ModInputsIntro)
* Splunk Javascript SDK: [SDK Site](http://dev.splunk.com/view/javascript-sdk/SP-CAAAECM)
* Modular Inputs with the SDK: [JS Modular Inputs](http://dev.splunk.com/view/javascript-sdk/SP-CAAAEXM)