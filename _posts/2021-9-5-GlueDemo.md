# A local Glue implementation based on https://aws.amazon.com/blogs/big-data/building-an-aws-glue-etl-pipeline-locally-without-an-aws-account/

# The Docker image is for Glue 1.0. Glue 2.0 uses the same Spark version
docker pull amazon/aws-glue-libs:glue_libs_1.0.0_image_01

# Launching a disposable container for interactive pyspark shell
docker run -it --rm amazon/aws-glue-libs:glue_libs_1.0.0_image_01 bash

# Launching a Notebook
docker run -it --rm -p 8888:8888 -p 4040:4040 -v ~/.aws:/root/.aws:ro amazon/aws-glue-libs:glue_libs_1.0.0_image_01 \
/home/jupyter/jupyter_start.sh















Questions
- What about port 4040?
- Read file from S3 - csv / Parquet
- Change data type of a column among allowed types: https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-pyspark-extensions-types.html

