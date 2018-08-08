# Secure Healthcare Backend

This serves as a bootstrapper and source for the Secure Backend Demo Application

# Setup

When you cloned the repo, you have to build the server from the swagger file using `swagger-node-codegen`.

To install the dependency:
```
npm install -g swagger-node-codegen
```

This installs the command `snc` as a global command.

# Building

Build the REST APIs from the swagger:
```
npm run-script build
```

This command generates the server code from the swagger file. All files will be generated under the `build` directory.

To start the server:
```
npm start
```
If something is wrong or is not up to date, update the `swagger.yaml` file.

Build the REST APIs from the swagger:
```
npm run-script build
```

Rinse and repeat.

Then you can start adding your application logic.

# Important Notes

- The command `npm run-script build` deletes the build directory. Until the command is updated, **use with caution** when adding application logic.
- The code use Javascript *Promises*. This will only work with Node >= v6.4. If you see `SyntaxError: Unexpected token` errors, it is likely that your Node JS is older.
- The `tests` folder contains naive cUrl-based requests to the server. This can be updated and improved.

# Editing the Swagger File

## Atom Editor

You can use the [Swagger Linter](https://atom.io/packages/linter-swagger).

## Smartbear Swagger Editor

### Online

You can visit this link: https://editor.swagger.io/

### Offline

You can use the Smartbear Swagger editor by setting up a server.

Pull the docker image:
```
docker pull swaggerapi/swagger-editor
```

Run the docker image as detached:
```
docker run -d -p 80:8080 swaggerapi/swagger-editor
```

## Console

You can use swagger-linter NPM module.

You can find more information in this link:
https://www.npmjs.com/package/swagger-cli

# Swagger Resources
- [Swagger Documentation](https://swagger.io/docs/specification/about/)

# TODO:
- [ ] Finalize Swagger file
- [ ] Add application logic folder in App
- [ ] Change the build script to copy the App to the server
- [ ] Add the scripts inside `tests` directory under 'test' in package.json
