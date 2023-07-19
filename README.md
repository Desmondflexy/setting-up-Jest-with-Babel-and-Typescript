# setting-up-Jest-with-Babel-and-Typescript

### Steps to setup Jest with Babel and Typescript
1. Create a new Node.js project and navigate to the project directory.

    ```
    yarn init --yes
    ```

2. Add the `scripts` property to the `package.json` file:
    ```javascript
    "scripts": {
      "test": "jest"
    }
    ```
3. Install the necessary dependencies:

    ```
    yarn add --dev jest @babel/core @babel/preset-env @babel/preset-typescript @types/jest
    ```
4. Create a `babel.config.js` file in the root directory of your project and add the following code:

    ```javascript
    module.exports = {
      presets: [
        ['@babel/preset-env', {targets: {node: 'current'}}],
        '@babel/preset-typescript',
      ],
    };
    ```
    This configuration tells Babel to use the `@babel/preset-env` and `@babel/preset-typescript` presets.

5. Run the command and reply the prompts:

    ```
    npx jest --init
    ```
    This creates the configuration file `jest.config.js` in the project root directory.

6. From the project root directory, run the command to create the test folder:
    ```
    mkdir __tests__
    ```
    This is where you should save all your test files which are named in the format `example.test.js` or `.ts`
