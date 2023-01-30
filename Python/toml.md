# TOML

[TOML](https://toml.io/en/) aims to be a minimal configuration file format that is easy to read due to obvious semantics, maps unambiguously to a hash table, and
is easy to parse into data structures in a wide variety of languages.

## config.toml

Create a config.toml file in your project directory.

```toml
setting1 = 'example1'
setting2 = 'example2'
setting3 = 'example3'
```
## python
```python
import toml

config = toml.load('config.toml')

setting1 = config['setting1']
setting2 = config['setting2']
setting3 = config['setting3']

print(setting1, setting2, setting3)
```