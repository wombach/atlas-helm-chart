# atlas-helm-chart
This chart will install the apache atlas and used solr for indexing and cassandra as backend storage.

To install the chart. clone the repo and run following command to install chart

```sh
helm install --name <any release name> -f atlas-helm-chart/values.yaml atlas-helm-chart
```

```sh
cd /home/wombach/helm/wombach
helm install --generate-name -f atlas-helm-chart/values.yaml atlas-helm-chart
```
This will run the solr, atlas, Cassandra and zookeeper pods

solr version : 7.5

atlas version : 2.1.0

cassandra version : 3.11.3

zookeeper version : 3.4.x

Download the Source code of Apache Atlas from here [Download](http://atlas.apache.org/Downloads.html)

## Build Atlas from source

```sh
tar xvfz apache-atlas-2.1.0-sources.tar.gz

cd apache-atlas-sources-2.1.0/

mvn clean -DskipTests install
```
## Packaging Apache Atlas
```sh
mvn clean -DskipTests package -Pdist
```
This will Generate tar file of Apache atlas
