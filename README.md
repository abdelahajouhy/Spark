*** Code Markdown ***
*********************
All projects with Sparks

# Java installation : 
java -version                                                                           <!-- check java version -->
apt install openjdk-8-jre                                                               <!-- install java -->
export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64                                      <!-- environment variable for java -->
echo "export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64 ">>.bash_rc                    <!-- bash_rc to keep after rebooting -->
echo $JAVA_HOME                                                                         <!--  check the environment variable -->
java -version
    openjdk version "1.8.0_352"
    OpenJDK Runtime Environment (build 1.8.0_352-8u352-ga-1~20.04-b08)
    OpenJDK 64-Bit Server VM (build 25.352-b08, mixed mode)

# Spark installation : 
wget https://archive.apache.org/dist/spark/spark-2.2.0/spark-2.2.0-bin-hadoop2.7.tgz    <!-- install Spark spark-2.2.0 -->
tar -xzf spark-2.2.0-bin-hadoop2.7.tgz                                                  <!-- dezip -->
sudo mv spark-2.2.0-bin-hadoop2.7 /opt/spark                                            <!-- move repo spark intp /opt/spark -->
export SPARK_HOME=/opt/spark                                                            <!--  environment variable for /opt/spark -->
export PATH=$SPARK_HOME/bin:$PATH                                                       <!--  environment variable for /opt/spark/bin -->
echo "export PATH=$SPARK_HOME/bin:$PATH ">>.bash_rc

# Python 3 installation :
sudo apt update
sudo apt-get install python3                                                            <!-- if fails, reboot the server -->
python3 --version                                                                       <!-- check version : current version 3.8.10 -->
export PYTHONPATH=$SPARK_HOME/python:$SPARK_HOME/python/lib/py4j-0.10.4-src.zip:$PYTHONPATH         
echo "export PYTHONPATH=$SPARK_HOME/python:$SPARK_HOME/python/lib/py4j-0.10.4-src.zip:$PYTHONPATH ">>.bash_rc
echo $PYTHONPATH
echo "export PYSPARK_PYTHON=python3 ">>.bash_rc


# Anaconda installation :
curl -O https://repo.anaconda.com/archive/Anaconda3-2019.03-Linux-x86_64.sh
chmod +x Anaconda3-2019.03-Linux-x86_64.sh 

# lauching Spark with Python3 :
/opt/spark/bin/pyspark                                                                     <!-- lanch the binary with python ./pyspark-->
      ____              __
     / __/__  ___ _____/ /__
    _\ \/ _ \/ _ `/ __/  '_/
   /__ / .__/\_,_/_/ /_/\_\   version 2.2.0
      /_/

Using Python version 3.8.10 (default, Nov 14 2022 12:59:47)                                <!-- Not the python version, it's the good one-->

# lauching Spark with Scala :
/opt/spark/bin/spark-shell 
      ____              __
     / __/__  ___ _____/ /__
    _\ \/ _ \/ _ `/ __/  '_/
   /___/ .__/\_,_/_/ /_/\_\   version 2.2.0
      /_/
         
Using Scala version 2.11.8 (OpenJDK 64-Bit Server VM, Java 1.8.0_352)                      <!--java -version: openjdk version "1.8.0_352"-->

