# efx-buttons-themelet

An example to use Liferay themelets.

## How to use themelets?
Themelets are small pieces of code, designed to provide styles or functionalities as npm packages, so you can search, choose the themelets you want to use, and extend your Liferay theme with it.

## How to create themelets?
The process to create a themelet is pretty simple by using the Yeoman Liferay Theme Generator, you only need to run the following command:
```
yo liferay-theme:themelet
```
It will ask you for some information about the themelet before creating it, like the desired name, ID, and which version of the Liferay Portal you intend to use. Also, it's possible to create one to be compatible with all versions of Liferay.

## How to publish themelets to npm?
First, you need to create an npm account, then run `npm login` on your terminal, and fill the credentials. If you want to test it worked, you can run the `npm whoami` command. It should return your npm username.
Then, to publish it, you need to execute the `npm publish` command. After that, your package should be available in the public npm registry to everyone who wanted to use it.
> For more information about npm packages and to understand how the semantic versioning works, you could check [here](https://docs.npmjs.com/getting-started/publishing-npm-packages).

## How to install the themelet on the theme?
Once you have the themelet published to npm, it is ready to extend your theme, and Liferay Theme Tasks have a gulp task for that.
To do this, you need to go to your theme directory and run `gulp extend` command, it will trigger an assistant to guide you through the import, you have to follow the steps and fill the information required. It should search the npm for the package you desire and proceed to the installation. After that, the themelet will be added to your `node_modules` folder, and your theme's `package.json` file will be modified to describe which themelets are installed.