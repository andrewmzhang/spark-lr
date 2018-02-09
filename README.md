
Run with

```
sbt package
./run.sh
```

Output from the run is captured in logger.txt

Output from my last run is in logger_old.txt

Here are my spark conf settings in spark/conf/spark-defaults.conf:
```
spark.driver.memory 25g
spark.driver.maxResultSize 0
spark.executor.memory 25g
```


To preprocess the data, run

```
python2 preprocess.py train.txt     # train.txt is from kaggle display advertising challenge
split -l 40000000 out.svm           # splits the data into xaa and xab, the training and test set, respectively 
```

Get the data from here: https://s3-eu-west-1.amazonaws.com/criteo-labs/dac.tar.gz
