# grundstuecksinformation-geoserver

DO NOT USE THIS! IN THIS STAGE IT'S NOT REALLY A FUNCTIONAL PART OF grundstuecksinformation.ch.


## Building the image
```
docker build -t sogis/grundstuecksinformation-geoserver:2.16.2 .
```

## Running 
```
docker run --rm --name grundstuecksinformation-geoserver -p 8888:8080 -v /tmp/data_dir:/var/local/geoserver sogis/grundstuecksinformation-geoserver
```

When mounting an empty `/tmp/data_dir` directory, there will be some errors during startup because of a missing `logging.xml` file. Fix #1: Use a `data_dir` from a vanilla geoserver install and delete the stuff you want get rid of.
