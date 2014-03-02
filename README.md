## ListIndices elasticsearch plugin

List all indices existing in an elasticsearch node.

### Install ListIndices

bin/plugin --url https://github.com/iterativ/elasticsearch-listindices/blob/master/binary/ListIndicesPlugin-1.0-SNAPSHOT.zip --install listindices

### Building & Installing ListIndices from source

```bash
$ mvn package
# in elasticsearch home
$ bin/plugin --url file:///<path-to-plugin>/target/releases/ListIndicesPlugin-1.0-SNAPSHOT-plugin.zip --install listindices
```

### Using ListIndices

Request indices:
```rest
GET /_indices
```

Example output:
```json
{
   "indices": [
      ".marvel-2014.02.26",
      ".marvel-2014.02.27",
      ".marvel-2014.02.28",
      ".marvel-2014.03.01",
      ".marvel-2014.03.02",
      "events",
      "haystack",
      "itemresults"
   ]
}
```