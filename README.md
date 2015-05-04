# df-cassandra-connector

The Cassandra Connector is an Actian DataFlow operator for querying and updating [Apache Cassandra](http://cassandra.apache.org/) databases.

## Configuration

Before building df-jsonpath-runner you need to define the following environment variables to point to the local DataFlow update site [dataflow-p2-site](https://github.com/ActianCorp/dataflow-p2-site) root directory and the DataFlow version.

    export DATAFLOW_REPO_HOME=/Users/myuser/dataflow-p2-site
    export DATAFLOW_VER=6.5.0.117

## Building

The update site is built using [Apache Maven 3.0.5 or later](http://maven.apache.org/).

To build, run:

    mvn clean install

## Using the Cassandra Connector with the DataFlow Engine

The build generates a JAR file in the target directory under
[df-cassandra-connector/cassandra-connector-op](https://github.com/ActianCorp/df-jsonpath/tree/master/jsonpath-op)
with a name similar to 

    cassandra-connector-op-1.y.z.jar

which can be included on the classpath when using the DataFlow engine.

## Installing the Cassandra Connector plug-in in KNIME

The build also produces a ZIP file which can be used as an archive file with the KNIME 'Help/Install New Software...' dialog.
The ZIP file can be found in the target directory under
[df-cassandra-connector/cassandra-connector-ui-top/update-site](https://github.com/ActianCorp/df-jsonpath/tree/master/jsonpath-ui-top/update-site) 
and with a name like 


    com.actian.ilabs.dataflow.cassandra.ui.update-1.y.z.zip

The file [examples/KNIME/JSONPath_Runner_Example.zip](https://github.com/ActianCorp/df-jsonpath/raw/master/examples/KNIME/JSONPath_Twitter_Example.zip) 
contains a KNIME workflow that can be imported into KNIME and used to test the plug-in.


