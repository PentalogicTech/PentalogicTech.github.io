
# study/getstudyurl()

>*Método que recibe el DNI + AN y devuelve la URL del estudio*


**Método:** *GET*


**URL:** *[https://pacs.diagnosticosalta.com.ar/api/study/getstudyurl.php](https://pacs.diagnosticosalta.com.ar/api/study/getstudyurl.php)*


**Authorization Token:** *(Solicitar)*


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


**URL:** *[https://pacs.diagnosticosalta.com.ar/api/study/getstudylist.php](https://pacs.diagnosticosalta.com.ar/api/study/getstudylist.php)*


**Authorization Token:** *(Solicitar)*


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


**URL:** *[https://pacs.diagnosticosalta.com.ar/api/study/getqrurl.php](https://pacs.diagnosticosalta.com.ar/api/study/getqrurl.php)*


**Authorization Token:** *(Solicitar)*


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


**URL:** *[https://pacs.diagnosticosalta.com.ar/api/worklist/create.php](https://pacs.diagnosticosalta.com.ar/api/worklist/create.php)*


**Authorization Token:** *(Solicitar)*


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


**URL:** *[https://pacs.diagnosticosalta.com.ar/api/worklist/list.php](https://pacs.diagnosticosalta.com.ar/api/worklist/list.php)*


**Authorization Token:** *(Solicitar)*


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


# studyxusuario/create()

>*Método que recibe datos de asignacion de usuario a estudio*


**Método:** *POST*


**URL:** *[https://pacs.diagnosticosalta.com.ar/api/studyxusuario/create.php](https://pacs.diagnosticosalta.com.ar/api/studyxusuario/create.php)*


**Authorization Token:** *(Solicitar)*


**Request:**

- Body Schema: application/json
```markdown
object
	accessionnumber: integer
	usuario_id: integer
```


**Responses:**

- **200 OK** - Response Schema: application/json
```markdown
result: Array of objects
  	Array [
	  studyxusuario_id: integer
        ]
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


# studyxusuario/update()

>*Método que recibe datos de modificacion asignacion de usuario a estudio*


**Método:** *POST*


**URL:** *[https://pacs.diagnosticosalta.com.ar/api/studyxusuario/update.php](https://pacs.diagnosticosalta.com.ar/api/studyxusuario/update.php)*


**Authorization Token:** *(Solicitar)*


**Request:**

- Body Schema: application/json
```markdown
object
	studyxusuario_id: integer
	accessionnumber: integer
	usuario_id: integer
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


# studyxusuario/delete()

>*Método que recibe datos de eliminacion asignacion de usuario a estudio*


**Método:** *POST*


**URL:** *[https://pacs.diagnosticosalta.com.ar/api/studyxusuario/delete.php](https://pacs.diagnosticosalta.com.ar/api/studyxusuario/delete.php)*


**Authorization Token:** *(Solicitar)*


**Request:**

- Body Schema: application/json
```markdown
object
	studyxusuario_id: integer
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