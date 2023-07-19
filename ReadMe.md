Steps to setup Jest with Babel and Typescript
Create a new Node.js project and navigate to the project directory.

yarn init --yes
Add the scripts property to the package.json file:

"scripts": {
  "test": "jest"
}
Install the necessary dependencies:

yarn add --dev jest @babel/core @babel/preset-env @babel/preset-typescript @types/jest
Create a babel.config.js file in the root directory of your project and add the following code:

module.exports = {
  presets: [
    ['@babel/preset-env', {targets: {node: 'current'}}],
    '@babel/preset-typescript',
  ],
};
This configuration tells Babel to use the @babel/preset-env and @babel/preset-typescript presets.

Run the command and reply the prompts:

npx jest --init
This creates the configuration file jest.config.js in the project root directory.

From the project root directory, run the command to create the test folder:

mkdir __tests__
This is where you should save all your test files which are named in the format example.test.js or .ts
