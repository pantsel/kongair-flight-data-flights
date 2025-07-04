## flights API

Provides the KongAir flights information including
flight number and other details.

### Specification

The API specification can be found in the [openapi.yaml](openapi.yaml) file.

### usage

The repository provides a `Makefile` with common usage.

#### To run unit tests

```
make test
```

#### To build the server

```
make build
```

#### To run the server on the default port

```
make run
```

In the `Makefile`, the default port is `8081`.

Alternatively the desired port can be passed to the built server executable directly,
for example:

```sh
./flights <port>
```

### Example client requests

Get all flights:
```
curl -s localhost:8081/flights
```

Get a specific flight by flight number:
```
curl localhost:8081/flights/KA0284
```

Get details for a specific flight by flight number:
```
curl localhost:8081/flights/KA0284/details
```

