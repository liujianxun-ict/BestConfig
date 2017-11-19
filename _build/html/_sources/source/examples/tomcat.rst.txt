.. BestConfig documentation master file, created by
   sphinx-quickstart on Tue Nov 14 10:53:55 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.
   
BestConf for Tomcat Server
==========================

Experimental Settings
---------------------

We executed Bestconf for the Tomcat server, and we applied sysbench to
test the performance of Tomcat server. All nodes used in our experiment
are shown below.

+-----------------+--------+-----------------------------------------+--------+ 
|   Node          |   OS   |                   CPU                   | Memory |
+=================+========+=========================================+========+ 
|  Tomcat Server  | CentOS | 16 Intel(R) Xeon(R) CPU E5620 @ 2.40GHz |  32GB  | 
+-----------------+--------+-----------------------------------------+--------+ 
|      JMeter     | CentOS | 16 Intel(R) Xeon(R) CPU E5620 @ 2.40GHz |  32GB  |
+-----------------+--------+-----------------------------------------+--------+

Performance Surface
-------------------

We use `JMeter`_ that is a widely adopted benchmark tools in the
workload generator for Tomcat to generate the target workload.

.. image:: ../pics/tomcat.png
  
.. raw:: html
   
   <p align="center">

	The performance surface of Tomcat under a page navigation workload.

.. raw:: html

   </p>

Test Results
------------

All the test resuls of Tomcat under different workloads ->
`Tomcat_Results`_.

Script files
------------

`Script files for Tomcat node`_\  `Scripts files for JMeter node`_

Interface Impl
--------------

The source files of `TomcatConfigReadin`_ and `TomcatConfigWrite`_
implement the interfaces of `ConfigReadin`_ and `ConfigWrite`_
respectively.

Download
--------

http://github.com/zhuyuqing/bestconf

.. _JMeter: http://jmeter.apache.org
.. _Tomcat_Results: https://github.com/zhuyuqing/bestconf/tree/master/testResults/tomcat
.. _Script files for Tomcat node: https://github.com/zhuyuqing/bestconf/tree/master/deploy/4Tomcat/scripts/scripts%20for%20Tomcat%20node
.. _Scripts files for JMeter node: https://github.com/zhuyuqing/bestconf/tree/master/deploy/4Tomcat/scripts/scripts%20for%20JMeter%20node
.. _TomcatConfigReadin: https://github.com/zhuyuqing/bestconf/blob/master/src/tomcat/cn/ict/zyq/bestConf/cluster/InterfaceImpl/TomcatConfigReadin.java
.. _TomcatConfigWrite: https://github.com/zhuyuqing/bestconf/blob/master/src/tomcat/cn/ict/zyq/bestConf/cluster/InterfaceImpl/TomcatConfigWrite.java
.. _ConfigReadin: https://github.com/zhuyuqing/bestconf/blob/master/src/main/cn/ict/zyq/bestConf/cluster/Interface/ConfigReadin.java
.. _ConfigWrite: https://github.com/zhuyuqing/bestconf/blob/master/src/main/cn/ict/zyq/bestConf/cluster/Interface/ConfigWrite.java