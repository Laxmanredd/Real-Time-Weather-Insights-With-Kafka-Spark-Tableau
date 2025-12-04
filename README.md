🌦️ Real-Time Weather Insights Dashboard
Kafka • Spark Structured Streaming • Tableau

This project implements a complete real-time data engineering pipeline that ingests, processes, aggregates, and visualizes weather data using modern big-data technologies.

🚀 Tech Stack

Apache Kafka – Real-time data ingestion

Apache Spark Structured Streaming – Real-time processing

Scala – Stream processing logic

Python – Kafka producer

Tableau – Interactive dashboard

CSV Storage – Exporting aggregated results

📡 Pipeline Architecture
Python Producer → Kafka Topic → Spark Structured Streaming → Aggregated Output → CSV → Tableau Dashboard

📝 Features

✔ Real-time weather streaming (temp, humidity, wind, AQI)
✔ Automatic schema parsing and data cleaning
✔ Live aggregation of average temperature by city
✔ Export results as a single CSV file
✔ Interactive Tableau dashboard with multiple charts
✔ Real-time filtering and drill-down insights

📁 Project Structure
📦 RealTime-Weather-Streaming-Pipeline
 ┣ 📜 producer.py
 ┣ 📜 spark_streaming.scala
 ┣ 📜 save_to_csv.scala
 ┣ 📜 README.md
 ┣ 📁 Tableau Dashboard (.twbx)

🧪 How to Run
1️⃣ Start Zookeeper
bin/zookeeper-server-start.sh config/zookeeper.properties

2️⃣ Start Kafka Broker
bin/kafka-server-start.sh config/server.properties

3️⃣ Create Topic
bin/kafka-topics.sh --create --topic temperature1 --bootstrap-server localhost:9092

4️⃣ Run Kafka Producer
python producer.py

5️⃣ Run Spark Streaming
spark-shell -i spark_streaming.scala

6️⃣ Export CSV

Run save_to_csv.scala

7️⃣ Load CSV into Tableau

Use exported TemperatureAvgCSV folder.

📊 Dashboard Preview

Includes:

Average Temperature by City

Temperature vs Humidity

Temperature Categories

Air Quality Comparison

Temperature vs Wind

🏁 Outcome

A complete real-time analytics system enabling automatic ingestion, processing, and visualization of weather insights for environmental decision-making.
