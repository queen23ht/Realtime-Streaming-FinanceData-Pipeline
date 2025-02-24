# RealTime-Streaming-FinanceData-Pipeline

Dự án này thiết lập một pipeline xử lý dữ liệu phân tán mạnh mẽ bằng cách sử dụng Apache Airflow để điều phối, Apache Kafka để xử lý luồng dữ liệu, Apache Spark để phân tích dữ liệu và Apache Cassandra để lưu trữ dữ liệu. Hệ thống được thiết kế để thu thập dữ liệu tài chính thời gian thực từ Finnhub API, xử lý và lưu trữ nhằm phục vụ phân tích.
## System Architecture

- **Apache Airflow**: Điều phối các luồng công việc trong pipeline dữ liệu.
- **Apache Kafka**: Quản lý dữ liệu đầu vào và đầu ra theo luồng.
- **Apache Spark**: Xử lý dữ liệu và thực hiện phân tích.
- **Apache Cassandra**: Lưu trữ dữ liệu đã được xử lý.
- **Docker**: Đóng gói từng thành phần trong container để đảm bảo tính độc lập và khả năng mở rộng.

## Directory Structure
```
finhub-data-pipeline/
│
├── docker-compose.yml
│
├── kafka/
│   └── kafka-init.sh
│
├── spark/
│   ├── Dockerfile
│   └── spark-job.py
│
├── airflow/
│   ├── Dockerfile
│   ├── dags/
│   │   └── finhub_ingest_dag.py
│   └── plugins/
│
└── cassandra/
    ├── init.cql
    └── Dockerfile
```
