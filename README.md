# poke config
An example, b&w internal config directory for the [poke tool](https://github.com/MrBananaLord/poke).

## Usage

1. install `poke-your-api` gem by running `gem install poke-your-api`
1. run `git clone https://github.com/BloomAndWild/poke-config.git`
1. run `mv poke-config/ ~/.poke`
1. Run `poke -e staging` and enjoy

(`bloomandwild/api/v2/availability/products` is a good candidate for testing)

### Environments
Enviroments can be set in the config file (i.e. `~/.poke/bloomandwild/config.json`). Use `poke -e env_name` to run the request against the specified environment.

Environments can be managed by the `poke env` command.

### Configuration
Configuration can be changed by creating `~/.poke.json` file.

```json
{
  "root_path": "/Users/janbator/.poke",
  "aliases": { 
    "health": "range-discovery/healthz",
    "range": "range-discovery/api/2023-08-15/range",
    "products": "bloomandwild/api/v2/availability/products",
  }
}
```

Aliases can be managed by the `poke alias` command.