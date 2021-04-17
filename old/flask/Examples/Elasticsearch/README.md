# Elasticsearch

##

```sh
virtualenv ./.venv
```

```sh
source ./.venv/bin/activate
```

```sh
pip3 install -r requirements.txt
```

## Test

```sh
curl localhost:9200/recipes/_search?q=title:salad -X GET
```
