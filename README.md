# zed-cargotom
## language server
https://github.com/frederik-uni/cargotom
## Config
```js
"lsp": {
    "cargotom": {
      "initialization_options": {
        "offline": false,
        "stable": false,
        "per_page_web": 50
      }
},
```

## Features
### Code actions
- "Make Workspace dependency" => This will generate `{ workspace = true }` for the dependency
- "Expand dependency specification" => This will convert from `"0.1.0"` to `{ version = "0.1.0" }`
- "Collapse dependency specification" => This will convert from `{ version = "0.1.0" }` to `"0.1.0`
- "Open Docs" => opens docs.rs/...
- "Open crates.io" => opens crates.io/...
- "Upgrade" => will upgrade the dependency version to the latest version
- "Upgrade All " => will upgrade every dependency version to the latest version
- "Update All" => will run `cargo run`

### Code completion
#### Dependencies
- crate names(online/offline)
- crate versions(online/offline)
- crate features(online/offline)
- feature key when version after the key `crate = "0.1.0"` => `crate = {ve"0.1.0"` to `crate = { version = "0.1.0" }`

### Diagnostics
- check if crate needs update
- check if crate version exists
- check if crate features exist
