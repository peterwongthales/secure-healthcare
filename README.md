# Secure Healthcare Backend

This is the source code of the Secure Backend Demo Application

To start the server:
```
npm start
```
If something is wrong or is not up to date, update the `swagger.yml` file.

Build the REST APIs from the swagger:
```
npm run-script build
```

Rinse and repeat.

## Setting up your local Swagger editor

```
docker pull swaggerapi/swagger-editor
docker run -d -p 80:8080 swaggerapi/swagger-editor
```

## TODO:
- [ ] Finalize Swagger file
- [ ] Separate to more manageable chunks
- [ ] Add application logic folder in App
- [ ] Change the build script to copy the App to the server
