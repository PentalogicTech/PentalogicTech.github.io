
# study/getstudyurl()

>*Método que recibe el DNI + AN y devuelve la URL del estudio*


**Método:** *GET*


**URL:** *[https://apigineco.pentalogic.tech/api/study/getstudyurl.php](http://apigineco.pentalogic.tech/api/study/getstudyurl.php)*


**Authorization Token:** *73e86c64-a8e4-4f79-87a2-f91aca93861d*


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


**URL:** *[https://apigineco.pentalogic.tech/api/worklist/create.php](https://apigineco.pentalogic.tech/api/worklist/create.php)*


**Authorization Token:** *73e86c64-a8e4-4f79-87a2-f91aca93861d*


**Request:**

- Body Schema: application/json
```markdown
object
	accion: string ['NW','CA']
	accessionnumber: string
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


**URL:** *[https://apigineco.pentalogic.tech/api/worklist/list.php](https://apigineco.pentalogic.tech/api/worklist/list.php)*


**Authorization Token:** *73e86c64-a8e4-4f79-87a2-f91aca93861d*


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
