# json-catalog
Add some azure-pipelines path patterns to https://www.schemastore.org/api/json/catalog.json. Go to https://www.schemastore.org/json/ for the original.

I am using this in Eclipse - YAML (Wild Web Developer) to have the code assist (autocomplete) enabled for Azure DevOps
pipelines.

To use this catalog, just set

https://raw.githubusercontent.com/osvetlik/json-catalog/develop/catalog.json

as the "URL of schema store catalog to use".

Currently, these patterns are supported:
```
        "azure-pipelines.yml",
        "azure-pipelines.yaml",
        ".azure-pipelines.yml",
        ".azure-pipelines.yaml",
        "azure-pipelines/**.yml",
        "azure-pipelines/**.yaml",
        ".azure-pipelines/**.yml",
        ".azure-pipelines/**.yaml"
```

I'm not sure about the `**` pattern, I assumed it will allow any number of folders in the path, but it only works
for files directly in the `azure-pipelines` or `.azure-pipelines` folder. Still, it's much better than the original.