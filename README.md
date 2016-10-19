Spark Practicals
====================================

#Pre-requisites:

* CDH 5.8 

#Setting up the environment


#Setting up the data 

In the `spark-practicals directory`:

Copy the test data from `spark-data` to hdfs:

	hdfs dfs -copyFromLocal spark-data 

_Note: Ingnore the warnings_


Verify that all the files are in hdfs:

	hdfs dfs -ls spark-data

Start pyspark within ipython notebook: 

	IPYTHON_OPTS="notebook" pyspark --packages com.databricks:spark-csv_2.10:1.3.0

#Assigments

1. WordCount using Apache Spark - open: WordCount.ipynb
2. Averrage Word Length using Apache Spark: open: AverageWordLength.ipynb
3. Average Temperature using Apache Spark - open: NSWAirTempeature.ipynb

#More info:

Contact: piotr.szul@csiro.au


 
