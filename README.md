# Purpose

Provide a script that makes it easy to generate a TPC-H data set and upload the output files to an AWS S3 bucket. 

The generated files are chunked to support the parallel load capabilities provided by Amazon Redshift, AWS Glue, AWS EMR, etc. 

The collection of files generated for each table are placed in their own S3 prefix which is necessary for certain services such as Redshift Spectrum. 


# Instructions

1. Clone the tpc-h dbgen utility

```sh
git clone https://github.com/electrum/tpch-dbgen

cd tpch-dbgen

make

cd..
```

2. Clone this project

```sh
git clone https://github.com/matwerber1/tpch-dbgen-to-aws-s3
```

3. Edit the configuration variables in run.sh (e.g. S3_BUCKET=???)

4. Run the script

```sh
cd tpch-dbgen-to-aws-s3
./run.sh
```
