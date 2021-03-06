# example-pages

## Installation

    npm install

## Directory structure

    dist/             #all the generated files live here
      bundled.css       #the bundled styles
      bundled.js        #the bundled scripts
      mocha.json        #the test output for consumption by Bamboo
      coverage/         #the full test coverage report
      
    src/              #all the source files live here
      assets/           #all the style and script files live here
        index.js          #the script entry file where you should write/require your code
        index.scss        #the style entry file where you should write/require your code
        package.json      #the dependency information for your styles, scripts and tests
        test/             #the script tests live here
         index.js     
         
    tasks/            #all the gulp tasks live here
    
    gulpfile.js       #the gulp entry file
    package.json      #the dependency information for the gulp tasks

## Build tasks

#### all

Run all the things!

    gulp all
    
You'll probably want to use this whenever you pull to get any new dependencies, and before you push to make sure you've
recorded all your dependencies, formatted your code appropriately and haven't caused any regressions.

#### default

Bundles the styles and scripts. 

    gulp

If you're not using the `watch` task you'll probably want to use this task whenever you change the code.

#### watch

Listens for changes to your style, script and package.json files and bundles/installs them when they change.

    gulp watch

You'll want to use this whenever you're making changes to the code.

#### clean

Deletes all the generated files from the `./dist` directory.

    gulp clean
    
Run this task when you want to re-bundle styles and scripts from a clean slate.

#### install

Install all the dependencies for your styles and scripts.

    gulp install
    
You'll probably want to run this after you or someone else makes changes the package.json file.

#### test

    gulp test

Run all the tests in PhantomJS.

#### debug

    gulp debug

Run a test server so you can debug the tests in the browser.

#### optimise

    gulp optimise

Optimise all the styles, scripts and assets.
    