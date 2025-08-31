# Spotify_Data_Insights
A serverless pipeline on AWS that turns raw Spotify CSVs into interactive dashboards.

Architecture
S3 (raw) → 2. Glue ETL (PySpark) → 3. S3 (curated Parquet) → 4. Glue Crawler + Catalog → 5. Athena SQL → 6. QuickSight dashboards

Contents

data/ → sample CSVs (albums.csv, artists.csv, tracks.csv)

Spotify Project.py → Glue ETL script

Spot_DE.png → architecture diagram

Demo assets → Athena & QuickSight snapshots

Quick Start

Upload CSVs → s3://your-raw-zone/

Run Glue Job → transform + write Parquet to s3://your-curated-zone/

Crawl Data → Glue Crawler → Data Catalog

Query in Athena → e.g. top artists, album trends, explicit vs clean tracks

Visualize in QuickSight → connect Athena dataset → build dashboard
