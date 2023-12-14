# Creating-Streaming-Data-Pipelines-using-Kafka
This is a simple project to create a data pipeline that collects the streaming data and loads it into a database.

# Scenario:

You are a data engineer at a data analytics consulting company. You have been assigned to a project that aims to de-congest the national highways by analyzing the road traffic data from different toll plazas. As a vehicle passes a toll plaza, the vehicle’s data like vehicle_id,vehicle_type,toll_plaza_id and timestamp are streamed to Kafka. Your job is to create a data pipe line that collects the streaming data and loads it into a database.

# Objectives
Create a streaming data pipe by performing these steps:
- Start a MySQL Database server.
- Create a table to hold the toll data.
- Start the Kafka server.
- Install the Kafka python driver.
- Install the MySQL python driver.
- Create a topic named toll in kafka.
- Download streaming data generator program.
- Customize the generator program to steam to toll topic.
- Download and customise streaming data consumer.
- Customize the consumer program to write into a MySQL database table.
- Verify that streamed data is being collected in the database table.

# Step 1: Preparation
wget https://archive.apache.org/dist/kafka/2.8.0/kafka_2.12-2.8.0.tgz
<img width="722" alt="image" src="https://github.com/kwagle7/Creating-Streaming-Data-Pipelines-using-Kafka/assets/13037108/967fc8c1-7221-4a8c-a518-4590c97b12a8">

# Start Zookeeper in a separate terminal
Zookeeper is required for Kafka to work. Start the Zookeeper server.
ZooKeeper is responsible for the overall management of Kafka cluster.
It monitors the Kafka brokers and notifies Kafka if any broker or partition goes down, or if a new broker or partition goes up.
<pre>
cd kafka_2.12-2.8.0
bin/zookeeper-server-start.sh config/zookeeper.properties
</pre>

# Start the kafka server on different terminal
Start a new terminal.
Run the commands below. This will start the Kafka message broker service.
<pre>
cd kafka_2.12-2.8.0
bin/kafka-server-start.sh config/server.properties
</pre>

# Create a topic
You need to create a topic before you can start to post messages.
to create a topic named news, start a new terminal and run the command below.
<pre>
cd kafka_2.12-2.8.0
bin/kafka-topics.sh --create --topic toll --bootstrap-server localhost:9092
</pre>

# Run the toll traffic simulator

<img width="642" alt="image" src="https://github.com/kwagle7/Creating-Streaming-Data-Pipelines-using-Kafka/assets/13037108/d740b5c1-c8ed-461c-8dec-e981e54fa42d">

# Configure and Run the streaming data reader

<img width="686" alt="image" src="https://github.com/kwagle7/Creating-Streaming-Data-Pipelines-using-Kafka/assets/13037108/5c1413aa-3382-4160-8be1-5cd114b152fa">

# Check whether the data is updated/write in operation or not:

<img width="468" alt="image" src="https://github.com/kwagle7/Creating-Streaming-Data-Pipelines-using-Kafka/assets/13037108/c66aea09-f2a8-45e3-b912-44dceedd9f3e">

Here, the streaming data is updated in the livetolldata table.
