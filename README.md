# -- DOCUMENTATION ENDPOINTS --

# GET - /

# Routing process

MAIN INDEX

```File: index.js```

In this file you will find the import (ES6) of the path like this
```
import api from './src/api/index.js';
```

and the use middleware method ```app.use()``` like this
```
app.use(api);
app.use('/api', api);
app.use('/api/v1', api);
```

In this way yo can see how is bringing the modules thata was exported throught the defaul export as you can see in the file ```'./src/api/index.js';``` in this way
```
export default router;
```

In this same file ```'./src/api/index.js';``` you will can find the Router mini app method whit the endpoint ```"/"``` and their respective callback that redirects to api docs or send api info like this

```
router.get('/', (req, res) => {
  // redirects to api docs or send api info
  res.json({
    name: packageConfig.name,
    apiVersion: packageConfig.version,
    repository: packageConfig.repository,
    description: packageConfig.description,
    license: packageConfig.license,
    licenseUrl: packageConfig.licenseUrl,
  });
});
```

