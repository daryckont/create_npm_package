# Steps to create and publish an NPM package

## Building the package
### Requirements

All you need to build (and then publish) an NPM package is the NPM command line tool which also goes by the name npm. 

Create the project directory, we will create a simple project which returns a hello string.

We create a new directory: `mkdir hello_foxy`

And then we move into that directory: `cd hello_foxy`
  
Initialize an NPM package

`npm init`
  
The command above should prompt an interactive session asking us to fullfil some questions about the package we want to create.
When we are done with the questions, a `package.json` file will be shown in the root of the project folder.
Note the _main_ field in the `package.json` file, it refers to the name of the file that would be loaded when your package is required by another application, by default it points to `index.js`.
  
Create an `index.js` file in the root of the project folder then add the code you wish it to run. For instance let's write a simple implementation that returns a `"Hello Foxy 🦊"` string.
  
Notice the **module.exports** at the bottom of the file, whatever you are exporting here is what would be available for importing when others install the package.
  
## Publishing the package
### Authenticate

You need to create an account in the NPM registry, you can do this [here](https://www.npmjs.com/).

After creating an account, go back to the command line and authenticate yourself with the command `npm login`, you would be prompted to provide your details, provide the required details and hit enter.

To test that the login was successful, enter the command `npm whoami`, your username should be logged to the CLI.

### Publish

Note that you may not be able to publish your package if someone else already has a package with the same name in the registry. You can simply change the name of the package to something unique to make it publishable.

Enter this command in the CLI:

`npm publish`

### Testing

To test the package, you simply need to install and use it. You can do the following to test the **hello-foxy** package:

Get into the _test_ folder and download the files, there is a simple test code inside the `test.js` file.

Execute the code in the `test.js` file using `node ./test.js`, you should see a friendly greeting in the console.

### Important Notes
> Note: Before you can publish private user-scoped npm packages, you must sign up for a paid npm user account.

> Additionally, to publish private organization-scoped packages, you must create an npm user account, then create a paid npm organization.

### Additional notes:

Adding a README to the project on NPM: [link](https://docs.npmjs.com/about-package-readme-files)

Versioning of NPM packages: [link](https://docs.npmjs.com/about-semantic-versioning)

Private NPM packages: [link](https://docs.npmjs.com/creating-and-publishing-private-packages)

NPM Package tutorial created with TypeScript: [link](https://medium.com/@nilayvishwakarma/build-an-npm-package-with-typescript-by-nilay-vishwakarma-f303d7072f80)




