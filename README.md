# Spark Course

## Introduction

The following repository contains the Jupyter Notebooks necessary for the Spark course. The course is divided in several sections, each one with its own notebook. The notebooks are numbered in the order they should be followed.

## Index

1. [Getting Started](#getting-started)
2. [Python Refresher](./notebooks/00_Python_Refresher.ipynb)
3. [Introduction to Spark](./notebooks/01_Introduction_to_Spark.ipynb)
4. [Spark Data Processing](./notebooks/02_Spark_Data_Processing.ipynb)
5. [Spark SQL](./notebooks/03_Spark_SQL.ipynb)
6. [Spark Performance Tuning](./notebooks/04_Spark_Performance_Tuning.ipynb)
   
## Getting Started

### 1. Install Java and Wget:

Spark requires the Java Runtime Environment (JRE) to run. If you don't already have Java installed, you can do it using `apt`:

```bash
sudo apt update
sudo apt install -y wget openjdk-11-jre-headless
```

Set the `JAVA_HOME` environment variable to the path where Java is installed:

```bash
echo "export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64" >> ~/.bashrc
source ~/.bashrc
```

### 2. Install Conda:

To run the notebooks, we will use a Conda environment. Execute the following commands that will download the Linux installer from the [official site](https://www.anaconda.com/download/) and install it:

```bash
wget https://repo.anaconda.com/archive/Anaconda3-2023.07-2-Linux-x86_64.sh
chmod +x Anaconda3-*-Linux-x86_64.sh
./Anaconda3-*-Linux-x86_64.sh
rm Anaconda3-*-Linux-x86_64.sh
```

Follow the prompts on the installer and accept the default settings. When finished, close and re-open your terminal window.

### 3. Create a Conda Environment:
 
Once Conda is installed, create a new environment for the course with the following command:

```bash
conda create -n pyspark python=3.8
```

Activate the created environment:

```bash
conda activate pyspark
```

### 4. Install PySpark and Required Libraries:

With the pyspark environment activated, install PySpark and other required libraries:

```bash
pip install pyspark jupyter jupyterlab
```

### 5. Clone this repository:

After the setup, clone this GitHub repository:

```bash
git clone git@github.com:amarchan-stratio/spark-course.git
cd spark-course/
```

### 5. Start Jupyter:

Navigate to the notebooks folder and start Jupyter notebook with:

```bash
cd notebooks/
jupyter lab
```