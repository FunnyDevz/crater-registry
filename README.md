# Crater Registry

A package registry for [crater](https://github.com/TheExeDEV/crater), the package manager for Luau and Roblox.

Browse packages: https://theexedev.github.io/crater-registry/

## Use this registry

Add it to `crater.config.json` in your project, or to your global config:

```json
{
  "registry": "github:TheExeDEV/crater-registry"
}
```

Then install packages as usual:

```bash
crater add scope/name^
```

## Publish a package

Every GitHub user owns one folder, named after their login in lowercase. If your login is `TheExeDEV`, your packages live in `theexedev/` and are named `theexedev/<package>`.

1. Fork this repository and clone your fork.
2. In your package, set `"name": "<your login>/<package>"` and `"can_publish": true` in `crater.json`.
3. Publish into the clone and open a pull request:

   ```bash
   crater publish --registry path/to/your/fork --pr
   ```

4. The **Check** workflow validates the pull request. A maintainer reviews and merges it.

After the merge the catalog and the website update automatically.

See [CONTRIBUTING.md](CONTRIBUTING.md) for the rules.
