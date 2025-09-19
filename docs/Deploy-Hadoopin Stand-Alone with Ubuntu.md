# ❇️ Deploy Hadoop in Stand-Alone with Ubuntu 24.04

<aside>
🍒

- September 2025
- on Ubuntu 22.04
- SSH Tools: Termius
</aside>

Once you’ve completed the prerequisites, log in as your `sudo` user to begin.

## Installing JDK

update package

```bash
sudo apt update
```

installing jdk

```bash
sudo apt insatall default-jdk -y
java -version
```

or

```bash
sudo apt install openjdk-8-jdk -y
java -version
```

## Install SSH(if not)

```bash
sudo apt install openssh-server openssh-client -y
```

## **Create a Dedicated Hadoop User**

```bash
sudo addgroup hadoop
sudo adduser --ingroup hadoop hduser
sudo su - hduser
```

### **Configure Passwordless SSH for hduser**

```bash
ssh-keygen -t rsa -P ""
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
chmod 640 ~/.ssh/authorized_keys
ssh localhost

```

## **Download and Extract Hadoop**

- https://hadoop.apache.org/releases.html
- hadoop-3.3.6

```bash
wget https://dlcdn.apache.org/hadoop/common/hadoop-3.3.6/hadoop-3.3.6.tar.gz
tar -xvzf hadoop-3.3.6.tar.gz
```

```bash
mv hadoop-3.3.6 hadoop
```

## **Configure Environment Variables**

Find **`JAVA_HOME`**

```bash
dirname $(dirname $(readlink -f $(which java)))
```

> my output: `/usr/lib/jvm/java-8-openjdk-amd64/jre`
> 

Edit ‎`~/.bashrc` and add:

```bash
vi ~/.bashrc
```

```bash
export HADOOP_HOME=~/hadoop
export JAVA_HOME=[your_java_home_path]
export PATH=$PATH:$HADOOP_HOME/bin:$HADOOP_HOME/sbin
```

Then run:

```bash
source ~/.bashrc
```

## **Configure Hadoop (Pseudo-Distributed Mode)**

Edit these files in ‎`~/hadoop/etc/hadoop/`:

```bash
vi ~/hadoop/etc/hadoop/hadoop-env.sh
```

- ‎`hadoop-env.sh`: Set ‎`JAVA_HOME`

If need, other configure:

‎`core-site.xml`, ‎`hdfs-site.xml`, ‎`mapred-site.xml`, ‎`yarn-site.xml`: Minimal configs for single-node operation.
See [official config guide ↗](https://hadoop.apache.org/docs/stable/hadoop-project-dist/hadoop-common/SingleCluster.html) for sample XML blocks. [⁠](https://hadoop.apache.org/docs/stable/hadoop-project-dist/hadoop-common/SingleCluster.html)

## **Format the Hadoop Filesystem**

```bash
hdfs namenode -format
```

## **Start Hadoop Services**

```bash
start-dfs.sh
start-yarn.sh
```

## **Test Your Installation**

```bash
hdfs dfs -mkdir /user/hduser
hadoop jar $HADOOP_HOME/share/hadoop/mapreduce/hadoop-mapreduce-examples-*.jar wordcount input output
```

<aside>
🍒

References：

- https://www.digitalocean.com/community/tutorials/how-to-install-hadoop-in-stand-alone-mode-on-ubuntu-20-04
- https://hadoop.apache.org/docs/current/hadoop-project-dist/hadoop-common/SingleCluster.html
- https://phoenixnap.com/kb/install-hadoop-ubuntu
</aside>
