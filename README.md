# molgenis-app-lifecycle-manuals
These are manuals to import source variables and harmonizations in MOLGENIS.

These manuals can be included in MOLGENIS as an app.

## Structure
The project sources are in the ```src``` folder. Within the src folder the following structure is needed to build the app.

- src
  - index.html
  - img
    - image.png

In the build config a config.json file is generated. You can alter it by updated this part of the ```webpack.config.js```

```javascript
plugins: [
  new GenerateJsonPlugin('config.json', {
    name: packageJson.name,
    label: packageJson.name,
    description: packageJson.description,
    version: packageJson.version,
    apiDependency: "v2",
    includeMenuAndFooter: true,
    runtimeOptions: {
      language: "en"
    }),
``` 

## Build
You can build the manuals by executing:

```
yarn build
```

It will generate a ```molgenis-app-lifecycle-manuals.zip``` in the ```dist``` directory. You can upload this file in MOLGENIS via the App-manager.