Steps to create and publish an NPM package.

. Create the project directory:
  mkdir "name of your project-directory"
  cd to project-directory
  
  Initialize an NPM package
  npm init
  
  The command above should prompt an interactive session asking us to fullfil some questions about the package we want to create.
  When we are done with the questions, a package.json file will be shown in the root of the project folder.
  Note the main field in the package.json file, it refers to the name of the file that would be loaded when your package is required by another application, by default it points toindex.js
  
  Create an index.js file in the root of the project folder then add the code you wish it to run. For instance let's write a simple implementation that returns a "Hello Foxy" string.
  
  Notice the module.exportsat the bottom of the file, whatever you are exporting here is what would be available for importing when others install the package.
  
  Publishing the package
Authenticate

You need to create an account in the NPM registry, you can do this here. If you are having any issues creating an account check the documentation here.

After creating an account, go back to the command line and authenticate yourself with the command npm login, you would be prompted to provide your details, provide the required details and hit enter.
To test that the login was successful, enter the command npm whoami, your username should be logged to the CLI.
Publish

Note that you may not be able to publish the random-number-package if someone else already has a package with the same name in the registry. You can simply change the name of the package to something unique to make it publishable. Check here for guides on naming a package.

Publishing your NPM package is as simple as entering this command in the CLI:

npm publish

Testing

To test the package, you simply need to install and use it. You can do the following to test the random-number-generator package:


Copy this simple test code and paste it in the test.jsfile.

const randomNumberGenerator = require('random-number-generator');console.log(randomNumberGenerator(5, 10));

Execute the code in the test.js file using node ./test.js, you should see a random number logged to the console.

Additional notes:

Adding a README to the project on NPM: https://docs.npmjs.com/about-package-readme-files
Versioning of NPM packages: https://docs.npmjs.com/about-semantic-versioning
Private NPM packages: https://docs.npmjs.com/creating-and-publishing-private-packages
Link to a npm package tutorial created with TypeScript: https://medium.com/@nilayvishwakarma/build-an-npm-package-with-typescript-by-nilay-vishwakarma-f303d7072f80


