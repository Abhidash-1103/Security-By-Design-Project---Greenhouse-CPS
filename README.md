SbD Greenhouse CPS

This project demonstrates a greenhouse cyber-physical system (CPS) built with Python and PySide, where sensors and PLCs (Programmable Logic Controllers) manage temperature, humidity, lighting, and irrigation.
It integrates with InfluxDB (for time-series data storage) and Grafana (for real-time dashboards). The system also includes attack simulation modules to study resilience and detection mechanisms.

Setup

1. Install dependencies

pip install PySide6 pyqtgraph influxdb


2. Run InfluxDB (v2.7.x)

cd .\path\to\influxdb
.\influxd


3.(Optional) Run Grafana

cd "C:\path\to\Grafana\bin"
.\grafana-server.exe


4.Set env variables

$env:INFLUXDB_URL="http://localhost:8086"
$env:INFLUXDB_ORG="your-org"
$env:INFLUXDB_BUCKET="your-bucket"
$env:INFLUXDB_TOKEN="your-token"

5.Usage

Start system GUI

python pyside.py


5. Simulate attacks

Override attack → inside pyside.py

DB injection attack →

python influx_attack.py

6. Visualization

PySide GUI → live system values

Grafana → dashboards & charts

Please checkout the ppt and report for the details.
