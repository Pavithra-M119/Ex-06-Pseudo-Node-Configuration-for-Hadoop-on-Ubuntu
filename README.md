# Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu

## AIM

To implement Pseudo Node configuration for Hadoop on ubuntu

## Pre-requisites

a) jdk

Single-Node Configuration

1.	Create a dedicated user account for hadoop
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/f864efe7-ac45-4385-89ea-f5957beb26c3)
   
2.	Install java1.8 in folder /usr/local
   ![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/2c1ef838-cfc8-4e6b-b6c5-a7ad6881ffd5)

3.	Install Hadoop
   ![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/1bddeadc-fa3d-48f9-9c49-519032f86708)

4.	Set the hadoop environment variables: Include the following lines in the
$HOME/.bashrc file
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/f863df0b-a92c-4e6f-b28d-30f5fdbe182c)

 
5.	Set hadoop environment variables: Include the following lines /etc/profile file
   ![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/295be481-7738-4c1f-90ad-a3f85bf2230a)
   ![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/404f2428-cc5e-440a-b265-9431e7ff7cbb)


6.	Run the.bashrc & profile files from the $ prompt for updating the changes
   ![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/4df0cf28-3532-4bd6-86bd-9a13679f0bb3)




$ bin/hadoop version	

7.	Configuration of the hadoop files: hadoop-env.sh, core-site.xml, mapred-site.xml, hdfs- site.xml and yarn-site.xml

path ::	/usr/local/hadoop-2.5.1/etc/hadoop

a)	hadoop-env.sh
Include the following lines in hadoop-env.sh file
export JAVA_HOME=/usr/local/jdk1.8.0_31
export HADOOP_PREFIX=/usr/local/hadoop-2.5.1



b)	core-site.xml
Configure the directory for Hadoop to store its data files, the network ports it listens to, etc. Setup will use Hadoop’s Distributed File System (HDFS-single local machine)
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/36a3630f-8100-4efb-935a-bc1abc535a91)


 
Include the following lines in core-site.xml file between <configuration> and
</configuration> tags
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/18cc249d-8500-4f6a-bab4-1929f5d9f421)


c)	mapred-site.xml

 ![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/cb351e03-73e4-44e8-b4c7-1dff09fe5ea9)


Include the following lines in mapred-site.xml file
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/d40160ac-8a4c-43a5-ab86-4c8af5d9b9a4)
 

d)	hdfs-site.xml
Include the following lines in hdfs-site.xml file
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/b7dc7a28-1219-46cf-a241-4b0dbfbc23bc)


e)	yarn-site.xml
Include the following lines in yarn-site.xml file
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/4df8f782-1181-4ba2-8b74-6844596a7668)

8.	Format the Hadoop File system implemented on top of the local file system using
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/f8e17485-6c9e-4e53-b75e-56188762dc2e)

9.	Start Hadoop using
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/3ae18af8-c215-472a-94aa-c8d4c6f86f24)


Explore Hadoop using http://localhost:50070/ from the browser	
 
10.	The commonly used HDFS Commands are as follows:
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/188abcc9-7917-4840-9a0e-096dd836d2b5)


11.	Create a directory ‘/input’ in HDFS
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/dfefd21b-aa18-4eb7-aae0-52e513ff18bc)


12.	Copy the input files into the distributed file system
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/dcc0d738-d144-4c19-86e2-363804a673c2)

13.	Run some of the examples provided
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/4e7449bc-1f1d-4c6b-8935-dacf01cdbd27)


14.	Examine the output files
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/df2ab599-f428-4391-924d-1a5a98e3f01b)

Copy the output files from the distributed file system to the local file system and examine them:
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/a10c301c-c48d-4fb2-b133-da03a5cec386)

 
or
View the output files on the distributed file system
![image](https://github.com/Pavithra-M119/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/119229774/32051be6-7caf-4a39-92a1-e0e87fe26835)

## Result:
Thus, the implementation of Pseudo Node configuration for Hadoop on ubuntu is successfully executed.
