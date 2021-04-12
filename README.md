# IDE_Streamsets_Spark_Jupyter
Use case IDE with Straemsets DataCollector, Streamsets Transformer, Jupyter Notebook and Standalone Spark cluster
## Start Spark session
### 1. Local spark session
```python
import pyspark
#from pyspark.sql import *
spark = pyspark.SparkContext(appName="Test")
```
### 2. Remote spark session
```python
import pyspark
from pyspark.sql import *
spark = SparkSession.builder.master("spark://spark-master:7077") \
                    .appName('docker-test-app') \
                    .getOrCreate()
```
