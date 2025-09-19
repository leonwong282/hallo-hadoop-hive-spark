<a id="readme-top"></a>

<div align="center">

# � Hello Hadoop Hive Spark

> Complete guide for deploying and managing Hadoop, Hive, and Spark clusters with practical data analysis projects

![Hadoop](https://img.shields.io/badge/Hadoop-3.4.1-yellow?style=for-the-badge&logo=apache)
![Hive](https://img.shields.io/badge/Hive-3.1.2-orange?style=for-the-badge&logo=apache)
![Spark](https://img.shields.io/badge/Spark-3.3.0-red?style=for-the-badge&logo=apache-spark)
![License](https://img.shields.io/badge/License-GPL--3.0-blue?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Linux-green?style=for-the-badge&logo=linux)

[🌍 English](README.md) | [🇹🇼 繁體中文](README.zh-TW.md) 

[Features](#-features) • [Quick-Start](#-quick-start) • [Deployment](#-deployment) • [Examples](#-examples) • [Contributing](#-contributing)

</div>

## 📸 Preview

![Hadoop Ecosystem Architecture](docs/images/hadoop-ecosystem.png)
*Complete Big Data ecosystem with Hadoop, Hive, and Spark integration*


## ✨ Features

- 🐘 **Hadoop 3.4.1**: Complete HDFS and MapReduce setup with high availability configuration
- 🏠 **Hive 3.1.2**: Data warehouse infrastructure with optimized queries and metadata management  
- ⚡ **Spark 3.3.0**: Unified analytics engine for large-scale data processing with SQL, streaming, and ML
- � **Cluster Deployment**: Automated scripts for multi-node cluster deployment
- 📊 **Practical Examples**: Real-world data analysis projects with sample datasets
- 🔧 **Common Commands**: Comprehensive reference for daily operations and administration
- � **Docker Support**: Containerized deployment options for development and testing
- 📚 **Step-by-Step Guides**: Detailed documentation from installation to production

## 🛠️ Tech Stack

- **Big Data Framework**: Apache Hadoop 3.4.1 (HDFS, MapReduce, YARN)
- **Data Warehouse**: Apache Hive 3.1.2 with Tez execution engine
- **Analytics Engine**: Apache Spark 3.3.0 (Core, SQL, Streaming, MLlib)
- **Database**: MySQL/PostgreSQL for Hive Metastore
- **Monitoring**: Ambari, Ganglia, Nagios for cluster monitoring
- **Development**: Jupyter Notebooks, Zeppelin for interactive analysis
- **Containerization**: Docker, Docker Compose for easy deployment
- **Languages**: Java 8/11, Scala 2.12, Python 3.7+, SQL

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## 🚀 Quick Start

### Prerequisites

Before you begin, ensure you have the following installed:

- **Operating System**: Ubuntu 20.04+ or CentOS 7+
- **Java**: OpenJDK 8 or 11
- **Memory**: At least 8GB RAM (16GB+ recommended for cluster)
- **Storage**: 50GB+ available disk space
- **Python**: Python 3.7+ for Spark PySpark
- **SSH**: SSH server configured for passwordless login

### Single Node Setup (Quick Start)

### Multi-Node Cluster Setup

For production deployment, see our comprehensive [Cluster Deployment Guide](docs/cluster-deployment.md).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## 📖 Deployment

### 🏗️ Architecture Overview

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Name Node     │    │   Resource      │    │   Spark Master  │
│   (HDFS Master) │    │   Manager       │    │                 │
│                 │    │   (YARN)        │    │                 │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         └───────────────────────┼───────────────────────┘
                                 │
    ┌────────────────────────────┼────────────────────────────┐
    │                            │                            │
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Data Node 1   │    │   Data Node 2   │    │   Data Node N   │
│   + Node Manager│    │   + Node Manager│    │   + Node Manager│
│   + Spark Worker│    │   + Spark Worker│    │   + Spark Worker│
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

### 🐘 Hadoop Configuration

**Core Components:**
- **HDFS**: Distributed file system for storing large datasets
- **MapReduce**: Distributed processing framework
- **YARN**: Resource management and job scheduling

**Key Configuration Files:**
- `core-site.xml` - Core Hadoop configuration
- `hdfs-site.xml` - HDFS configuration  
- `mapred-site.xml` - MapReduce configuration
- `yarn-site.xml` - YARN configuration

### 🏠 Hive Configuration

**Features:**
- SQL-like queries on large datasets
- Schema on read capability
- Integration with Hadoop ecosystem
- Support for various file formats (Parquet, ORC, Avro)

**Configuration:**
- `hive-site.xml` - Hive configuration
- Metastore database setup (MySQL/PostgreSQL)
- Tez execution engine for better performance

### ⚡ Spark Configuration

**Components:**
- **Spark Core**: Basic functionality and RDDs
- **Spark SQL**: Structured data processing
- **Spark Streaming**: Real-time stream processing  
- **MLlib**: Machine learning library

**Execution Modes:**
- Standalone cluster mode
- YARN cluster mode
- Local mode for development

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## 📊 Examples

### Example 1: Word Count with Hadoop MapReduce


### Example 2: Data Analysis with Hive


### Example 3: Real-time Processing with Spark


### Example 4: Machine Learning with Spark MLlib

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Quick Contribution Steps

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/NewDeploymentGuide`)
3. Commit your changes (`git commit -m 'Add deployment guide for AWS'`)
4. Push to the branch (`git push origin feature/NewDeploymentGuide`)
5. Open a Pull Request

### Areas for Contribution

- **Deployment Scripts**: Cloud-specific deployment guides (AWS, GCP, Azure)
- **Performance Tuning**: Configuration optimization guides
- **Use Cases**: Real-world data analysis examples
- **Documentation**: Tutorials and best practices
- **Bug Fixes**: Issues with installation or configuration

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## 📋 Roadmap

- [ ] **v2.0**: Cloud deployment templates (AWS, GCP, Azure)
- [ ] **v2.1**: Kubernetes deployment with Helm charts  
- [ ] **v2.2**: Integration with Apache Kafka for real-time pipelines
- [ ] **v2.3**: Machine learning workflow examples with MLflow
- [ ] **v2.4**: Data governance with Apache Atlas integration
- [ ] **v2.5**: Advanced monitoring with Prometheus and Grafana

See the [open issues](https://github.com/leonwong282/hello-hadoop-hive-spark/issues) for a full list of proposed features and known issues.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## 📄 License

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## 👥 Authors

- **Leon Wong** - *Initial work* - [leonwong282](https://github.com/leonwong282)

See also the list of [contributors](https://github.com/leonwong282/hello-hadoop-hive-spark/contributors) who participated in this project.

## 🙏 Acknowledgments

This project was inspired by and built upon the work of many excellent open source projects and communities. We are grateful to:

### � Big Data Ecosystem
- **[Apache Hadoop](https://hadoop.apache.org/)** - The foundation of modern big data processing
- **[Apache Hive](https://hive.apache.org/)** - Data warehouse infrastructure built on Hadoop
- **[Apache Spark](https://spark.apache.org/)** - Unified analytics engine for large-scale data processing
- **[Apache Tez](https://tez.apache.org/)** - Extensible framework for building high-performance batch applications

### 📚 Documentation & Learning Resources
- **[Hadoop: The Definitive Guide](https://www.oreilly.com/library/view/hadoop-the-definitive/9781491901687/)** - Comprehensive Hadoop reference
- **[Learning Spark](https://www.oreilly.com/library/view/learning-spark-2nd/9781492050032/)** - Modern Spark development guide
- **[Programming Hive](https://www.oreilly.com/library/view/programming-hive/9781449326944/)** - Complete Hive programming guide

### �️ Development & Deployment Tools
- **[Cloudera](https://www.cloudera.com/)** - Enterprise data platform and distributions
- **[Hortonworks](https://www.cloudera.com/products/hdp.html)** - Open source big data platform (now part of Cloudera)
- **[Apache Ambari](https://ambari.apache.org/)** - Management and monitoring platform
- **[Docker](https://www.docker.com/)** - Containerization platform for easy deployment

### 🌟 Community & Open Source
- **Apache Software Foundation** - For maintaining these incredible open source projects
- **Big Data Community** - For continuous innovation and knowledge sharing
- **Stack Overflow Contributors** - For solving countless deployment and configuration issues
- **GitHub Community** - For collaboration and code sharing

---

*If you're using this project in production or for learning, we'd love to hear about your experience! Feel free to [share your story](https://github.com/leonwong282/hello-hadoop-hive-spark/discussions).*

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## 📞 Support

If you have any questions or need help, please:

- 📝 [Open an issue](https://github.com/leonwong282/hello-hadoop-hive-spark/issues/new)
- 💬 [Start a discussion](https://github.com/leonwong282/hello-hadoop-hive-spark/discussions)
- 📧 Email us at: leonwong282@gmail.com
- 📖 Check our [documentation](docs/)
- 🔍 Search existing [issues](https://github.com/leonwong282/hello-hadoop-hive-spark/issues)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## 🔗 Useful Links

- **🌐 Web UIs**: 
  - Hadoop NameNode: http://localhost:9870
  - YARN ResourceManager: http://localhost:8088  
  - Spark Master: http://localhost:8080
  - Spark History Server: http://localhost:18080
- **📚 Official Documentation**:
  - [Hadoop Documentation](https://hadoop.apache.org/docs/)
  - [Hive Documentation](https://hive.apache.org/documentation.html)
  - [Spark Documentation](https://spark.apache.org/docs/latest/)
- **🎓 Learning Resources**:
  - [Hadoop Tutorial](https://hadoop.apache.org/docs/stable/hadoop-project-dist/hadoop-common/SingleCluster.html)
  - [Spark Quick Start](https://spark.apache.org/docs/latest/quick-start.html)
  - [Hive Tutorial](https://cwiki.apache.org/confluence/display/Hive/Tutorial)

---

<div align="center">

**⭐ Star this repository if it helped you build your big data cluster!**

Made with ❤️ for the Big Data Community by [Leon](https://github.com/leonwong282)

</div>
