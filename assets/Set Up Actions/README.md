<p align="center"> 🤖 Setting Up Your Environment
    <br> 
</p>

## 📝 Table of Contents

- [Steps](#steps)
- [Images](#demo)


## 🧐 About <a name = "about"></a>

- 1. Run Ad Manager

    export SPARK_KAFKA_VERSION=0.10

    spark-submit --packages org.apache.spark:spark-sql-kafka-0-10_2.11:2.4.5 ad_manager.py 18.211.252.152:9092 de-capstone1 ec2-54-145-108-208.compute-1.amazonaws.com root 123 upgrad
- 3. Run Ad Server

    python ad_server.py ec2-54-145-108-208.compute-1.amazonaws.com root 123 upgrad
- 4. Run User Sim

    python user simulator.py ec2-54-145-108-208.compute-1.amazonaws.com root 123 upgrad http 0.0.0.0 5000 0.0.0.0 8000
- 5. Run Feedback Handler

    python feedback handler.py 127.0.0.1:9092 user-feedback ec2-54-145-108-208.compute-1.amazonaws.com root 123 upgrad
- 6. Run User Feedback Writer

    export SPARK_KAFKA_VERSION=0.10

    #Change the path and checkpoint in python file if running again.

    spark-submit --packages org.apache spark:spark-sql-kafka-0-10_2.11:2.4.5 user feedback_writer.py 127.0.0.1 9092 user-feedback

    Hadoop ts -Is /home/hadoop/op11

## 🎥 Demo / Working <a name = "demo"></a>

![Working](https://media.giphy.com/media/20NLMBm0BkUOwNljwv/giphy.gif)

