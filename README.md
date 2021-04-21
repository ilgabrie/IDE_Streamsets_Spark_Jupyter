# IDE_Streamsets_Spark_Jupyter_Zeppelin
Use case IDE with Straemsets DataCollector, Streamsets Transformer, Jupyter Notebook, Zeppelin notebook server and Standalone Spark cluster
## Access of WebUIs
- Zeppelin http://tsi-ucf-ide.westeurope.cloudapp.azure.com:8088
- Jupyter http://tsi-ucf-ide.westeurope.cloudapp.azure.com:8888
- Spark master UI http://tsi-ucf-ide.westeurope.cloudapp.azure.com:8080
- Streamsets DataCollector http://tsi-ucf-ide.westeurope.cloudapp.azure.com:18630
- Streamsets Transformer http://tsi-ucf-ide.westeurope.cloudapp.azure.com:19630
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
