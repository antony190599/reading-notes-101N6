# 🚀 Extracción de Datos desde SQL a AWS S3 en CSV

## 🔹 **Arquitectura General**
Para crear un sistema que extraiga datos desde una base de datos SQL y los almacene como archivos CSV en AWS, seguimos estos pasos:

1. **Origen de Datos:** Base de datos SQL (MySQL, PostgreSQL, SQL Server, etc.).
2. **Extracción:** Un script en Python con `pandas` y `SQLAlchemy` para extraer datos.
3. **Transformación (Opcional):** Limpieza y procesamiento con Pandas o PySpark.
4. **Carga en AWS:** Guardar los CSV en Amazon S3 mediante `boto3`.
5. **Automatización:** Usar AWS Lambda, Step Functions o una instancia EC2 con un cron job.

---

## 🔹 **Implementación Técnica**
### **1️⃣ Conectar a la base de datos y extraer datos**
```python
import pandas as pd
import sqlalchemy

# Parámetros de conexión
DB_TYPE = 'postgresql'  # O 'mysql', 'mssql+pyodbc', etc.
DB_HOST = 'tu_host'
DB_PORT = '5432'
DB_NAME = 'tu_base_de_datos'
DB_USER = 'tu_usuario'
DB_PASS = 'tu_contraseña'

# Crear la conexión con SQLAlchemy
engine = sqlalchemy.create_engine(f"{DB_TYPE}://{DB_USER}:{DB_PASS}@{DB_HOST}:{DB_PORT}/{DB_NAME}")

# Ejecutar consulta y cargar datos en un DataFrame
query = "SELECT * FROM tu_tabla"
df = pd.read_sql(query, engine)

# Guardar como CSV
csv_path = "/tmp/datos.csv"  # Se guarda temporalmente antes de subir a AWS
df.to_csv(csv_path, index=False)
```
## **2 Subir a Amazon S3 con boto3**
```
import boto3

# Configurar AWS
AWS_ACCESS_KEY = "tu_access_key"
AWS_SECRET_KEY = "tu_secret_key"
BUCKET_NAME = "tu-bucket"
S3_FILENAME = "data/datos.csv"  # Ruta dentro del bucket

# Inicializar cliente de S3
s3_client = boto3.client(
    's3',
    aws_access_key_id=AWS_ACCESS_KEY,
    aws_secret_access_key=AWS_SECRET_KEY
)

# Subir archivo CSV a S3
s3_client.upload_file(csv_path, BUCKET_NAME, S3_FILENAME)

print("Archivo subido exitosamente a S3")
```
## **3️⃣ Automatización con AWS Lambda**
Si quieres que esto corra automáticamente, puedes:

- Crear una función Lambda en AWS y subir el script (zip con boto3 y sqlalchemy).
- Programar la ejecución con EventBridge (por ejemplo, cada día a las 12 AM).
- Usar AWS Secrets Manager para gestionar credenciales de la base de datos.
## **🔹 Alternativas Mejoradas**
- Si los datos son grandes, usa AWS Glue para transformar y almacenar en S3 en formato Parquet.
- Para automatización avanzada, usa AWS Step Functions en vez de Lambda.
- Si quieres análisis en tiempo real, considera AWS Kinesis en vez de CSV.

