Spark Practicals
====================================

#Assigments

Start pyspark within ipython notebook: 

    IPYTHON_OPTS="notebook" pyspark --packages com.databricks:spark-csv_2.10:1.3.0


1. WordCount using Apache Spark - open: `WordCount.ipynb`
2. Averrage Word Length using Apache Spark: open: `AverageWordLength.ipynb`
3. Average Temperature using Apache Spark - open: `NSWAirTempeature.ipynb`



#Setting up CDH distribution

* CDH 5.8 

##Setting up the environment

This is somewhat lenghty setup process need to install python2.7 on CentoOS.

Sudo to the root:

	sudo su -


Install python build dependencies:

	yum groupinstall "Development tools"
    yum install zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gdbm-devel db4-devel libpcap-devel xz-devel
    

Download, build and install python2.7:

 	wget https://www.python.org/ftp/python/2.7.12/Python-2.7.12.tgz
    tar -xzf Python-2.7.12.tgz 
    cd Python-2.7.12
	./configure --prefix=/usr/local --enable-unicode=ucs4 --enable-shared LDFLAGS="-Wl,-rpath /usr/local/lib"
	make && make altinstall


Install pip: 

	wget https://bootstrap.pypa.io/get-pip.py
	python2.7 get-pip.py 

Install virtualenv:

	pip install virtualenv


EXIT root mode:

	exit

_Pause and make sure you are not longer root user._


Create and activate python virtual environment named `pyspark`:

   	virtualenv pyspark
   	source ~/pyspark/bin/activate

Install required packages:

    pip install numpy pandas jupyter


##Setting up the data 

In the `spark-practicals` directory:

Copy the test data from `spark-data` to hdfs:

	hdfs dfs -copyFromLocal spark-data 

_Note: Ingnore the warnings_


Verify that all the files are in hdfs:

	hdfs dfs -ls spark-data

#More info:

Contact: piotr.szul@csiro.au


 
