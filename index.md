
# study/getstudyurl()

>*Método que recibe el DNI + AN y devuelve la URL del estudio*


**Método:** *GET*


**URL:** *[http://api.pentalogic.tech/study/getstudyurl.php](http://api.pentalogic.tech/study/getstudyurl.php)*


**Authorization Token:** *d7b3a04d-e8c9-498f-ab51-625b1f920960*


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


# study/getstudylist()

>*Método que recibe el DNI + Fecha Desde + Fecha Hasta y devuelve el listado de estudios*


**Método:** *GET*


**URL:** *[http://api.pentalogic.tech/study/getstudylist.php](http://api.pentalogic.tech/study/getstudylist.php)*


**Authorization Token:** *d7b3a04d-e8c9-498f-ab51-625b1f920960*


**Parámetros:** 
- pat_id - integer
- fecha_desde - date
- fecha_hasta - date

**Responses:**

- **200 OK** - Response Schema: application/json
```markdown
result: Array of objects
  	Array [
   	  pat_id: integer,
			study_datetime: datetime,
			accession_no: string,
			study_desc: string,
			mods_in_study: string,
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

# study/getqrurl()

>*Método que recibe el DNI + AN y devuelve la URL del acceso al portal via código QR*


**Método:** *GET*


**URL:** *[http://api.pentalogic.tech/study/getqrurl.php](http://api.pentalogic.tech/study/getqrurl.php)*


**Authorization Token:** *d7b3a04d-e8c9-498f-ab51-625b1f920960*


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

# study/getinformeurl()

>*Método que recibe el DNI + AN y devuelve un array con las URL de los informes vinculados al estudio*


**Método:** *GET*


**URL:** *[http://api.pentalogic.tech/study/getinformeurl.php](http://api.pentalogic.tech/study/getqrurl.php)*


**Authorization Token:** *d7b3a04d-e8c9-498f-ab51-625b1f920960*


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


**URL:** *[http://api.pentalogic.tech/worklist/create.php](http://api.pentalogic.tech/worklist/create.php)*


**Authorization Token:** *d7b3a04d-e8c9-498f-ab51-625b1f920960*


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
	telefono: string
	email: string
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


**URL:** *[http://api.pentalogic.tech/worklist/list.php](http://api.pentalogic.tech/worklist/list.php)*


**Authorization Token:** *d7b3a04d-e8c9-498f-ab51-625b1f920960*


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
		telefono: string
		email: string
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
