.. BestConfig documentation master file, created by
   sphinx-quickstart on Tue Nov 14 10:53:55 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.
   
BestConf for Cassandra
======================


Experimental Settings
---------------------

We executed Bestconf for the spark cluster with 4 nodes. The spark
cluster consists of 1 master node and 3 slave nodes. All nodes used in
our experiment are shown below.

+-------------+--------+-----------------------------------------+--------+ 
|   Node      |   OS   |                   CPU                   | Memory |
+=============+========+=========================================+========+ 
| Cassandra 1 | CentOS | 16 Intel(R) Xeon(R) CPU E5620 @ 2.40GHz |  32GB  | 
+-------------+--------+-----------------------------------------+--------+ 
| Cassandra 2 | CentOS | 16 Intel(R) Xeon(R) CPU E5620 @ 2.40GHz |  32GB  |
+-------------+--------+-----------------------------------------+--------+
| Cassandra 3 | CentOS | 16 Intel(R) Xeon(R) CPU E5620 @ 2.40GHz |  32GB  |
+-------------+--------+-----------------------------------------+--------+ 
|    YCSB     | CentOS | 16 Intel(R) Xeon(R) CPU E5620 @ 2.40GHz |  32GB  |
+-------------+--------+-----------------------------------------+--------+


Performance Surface
-------------------

We use `YCSB`_ that is a widely adopted benchmark tools in the workload
generator for Cassandra to generate the target workload. Currently, the
workload adopted in our test is workoada, and we set recorecount to
17000000 and operationcount to 720000. Figure 1 is the scatter plot of
performance for Cassandra under YCSB workloada.


.. image:: ../pics/cassandra-scatter.jpg
  
.. raw:: html
   
   <p align="center">

	The scatter plot of performance for Cassandra under YCSB workloada.

.. raw:: html

   </p>

Test Results
------------

The test result of Cassandra under YCSB workloada
`cassandraYcsba.arff`_.

Interface Impl
--------------

The source files of `CassandraConfigReadin`_ and `CassandraConfigWrite`_
implement the interfaces of `ConfigReadin`_ and `ConfigWrite`_
respectively.

Download
--------

http://github.com/zhuyuqing/bestconf

.. _YCSB: https://github.com/brianfrankcooper/YCSB
.. _cassandraYcsba.arff: https://github.com/zhuyuqing/bestconf/blob/master/testResults/cassandra/cassandraYcsba.arff
.. _CassandraConfigReadin: https://github.com/zhuyuqing/bestconf/blob/master/src/cassandra/cn/ict/zyq/bestConf/cluster/InterfaceImpl/CassandraConfigReadin.java
.. _CassandraConfigWrite: https://github.com/zhuyuqing/bestconf/blob/master/src/cassandra/cn/ict/zyq/bestConf/cluster/InterfaceImpl/CassandraConfigWrite.java
.. _ConfigReadin: https://github.com/zhuyuqing/bestconf/blob/master/src/main/cn/ict/zyq/bestConf/cluster/Interface/ConfigReadin.java
.. _ConfigWrite: https://github.com/zhuyuqing/bestconf/blob/master/src/main/cn/ict/zyq/bestConf/cluster/Interface/ConfigWrite.java