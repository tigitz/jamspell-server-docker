# JamSpell HTTP API Server Docker Container

A docker container for the [JamSpell HTTP API Server](https://github.com/bakwc/JamSpell#http-api) with `en` data model
preloaded.

## Environment Configuration
| Environment Variable  | Description | Default Value |
| ------------- | ------------- | ------------- |
| HOST  | Bind interface for the server  | `0.0.0.0` |
| PORT  | Port to expose server on  | `8080` |
| DATA_DIR | Directory where models are mounted | `/opt/jamspell/data` |
| MODEL | Model file to use from `DATA_DIR` | `en.bin` |

## Example Usage
```sh
$  docker run --rm -it tigitz/jamspell
+ /usr/bin/jamspell-server /opt/jamspell/data/en.bin 0.0.0.0 8080
[info] loading model
[info] starting web server at 0.0.0.0:8080
```

Or you can use your own data model
```sh
$  docker run --rm -it -v `pwd`/en.bin:/opt/jamspell/data/en.bin tigitz/jamspell
```
