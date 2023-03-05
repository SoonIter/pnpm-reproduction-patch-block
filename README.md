# reproduction of patch error block
this is a quick demo to test pnpm behavior

```
├── node_modules
├── package.json
├── packages
│   └── a
│       ├── node_modules
│       └── package.json  -->>  @dagrejs/graph@2.1.11
├── patches
│   └── @dagrejs__graphlib@2.1.11.patch
├── pnpm-lock.yaml
└── pnpm-workspace.yaml
```

1. run `pnpm install` or `pd install`(dev)

2. modify the `package.json` 

```json
"dependencies": {
    "vue": "3.2.0" // add one line dependency or something else
},
```

3. rerun  `pnpm install`