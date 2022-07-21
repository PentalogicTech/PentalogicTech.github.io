
# study/getstudyurl()

>*Método que recibe el DNI + AN y devuelve la URL del estudio*


**Método:** *GET*


**URL:** *[https://apifisika.pentalogic.tech/api/study/getstudyurl.php](http://apifisika.pentalogic.tech/api/study/getstudyurl.php)*


**Authorization Token:** *b0f4f0c9-f404-47fd-b62c-8094e2c78c6a*


**Parámetros:** 
- pat_id - integer
- accession_no - integer


**Responses:**

- **200 OK** - Response Schema: application/json
```markdown
result: Array of objects
  	Array [
   	  url: string
        ]
```	
- **200 OK** - Response Schema: application/json
```markdown
   result: object	
	message: string
```	
- **400 Bad Request** - Response Schema: application/json
```markdown
   resultError: object	
	message: string
```
- **401 Unauthorized token** - Response Schema: application/json
```markdown
   resultError: object	
	message: string
```
<br>
<br>
<br>

# worklist/create()

>*Método que recibe datos de un ingreso de paciente e inserta en la cola de envío al servidor de worklist*


**Método:** *POST*


**URL:** *[https://apifisika.pentalogic.tech/api/worklist/create.php](https://apifisika.pentalogic.tech/api/worklist/create.php)*


**Authorization Token:** *b0f4f0c9-f404-47fd-b62c-8094e2c78c6a*


**Request:**

- Body Schema: application/json
```markdown
object
	accion: string ['NW','CA']
	accessionnumber: integer
	modalidad: string ['CR','MR','CT','US','DX','MG','NM','NN']
	estudio: string
	apellido: string
	nombre: string
	dni: integer
	fechanac: integer ['YYYYMMDD']
	sexo: string ['M','F']
	aetitle: string
```


**Responses:**

- **200 OK** - Response Schema: application/json
```markdown
   result: object	
	message: string
```	
- **503 Service Unavailable** - Response Schema: application/json
```markdown
   resultError: object	
	message: string
```
- **400 Bad Request** - Response Schema: application/json
```markdown
   resultError: object	
	message: string
```
- **401 Unauthorized token** - Response Schema: application/json
```markdown
   resultError: object	
	message: string
```
<br>
<br>
<br>

# worklist/list()

>*Método que permite listar los registros que se encuentran en la cola de envío a worklist, en estado pendiente*


**Método:** *GET*


**URL:** *[https://apifisika.pentalogic.tech/api/worklist/list.php](https://apifisika.pentalogic.tech/api/worklist/list.php)*


**Authorization Token:** *b0f4f0c9-f404-47fd-b62c-8094e2c78c6a*


**Responses:**

- **200 OK** - Response Schema: application/json
```markdown
result: Array of objects
  	Array [
   	  accion: string ['NW','CA']
	  accessionnumber: integer
	  modalidad: string ['CR','MR','CT','US','DX','MG','NM','NN']
	  estudio: string
	  apellido: string
	  nombre: string
	  dni: integer
	  fechanac: integer ['YYYYMMDD']
	  sexo: string ['M','F']
	  aetitle: string
        ]
```	
- **200 OK** - Response Schema: application/json
```markdown
   result: object	
	message: string
```	
- **401 Unauthorized token** - Response Schema: application/json
```markdown
   resultError: object	
	message: string
```
<br>
<br>
<br>
