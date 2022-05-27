
# study/getstudyurl()
Implementación para Clinica del Pilar
>*Método que recibe el DNI + AN y devuelve la URL del estudio*


**Método:** *GET*


**URL:** *[https://pacs.clinicadelpilartuc.com.ar/api/study/getstudyurl.php](https://pacs.clinicadelpilartuc.com.ar/api/study/getstudyurl.php)*


**Authorization Token:** *871b2cd8-6018-46ed-9490-f86ec77fa4e2*


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
Implementación para Clinica del Pilar
>*Método que recibe datos de un ingreso de paciente e inserta en la cola de envío al servidor de worklist*


**Método:** *POST*


**URL:** *[https://pacs.clinicadelpilartuc.com.ar/api/worklist/create.php](https://pacs.clinicadelpilartuc.com.ar/api/worklist/create.php)*


**Authorization Token:** *871b2cd8-6018-46ed-9490-f86ec77fa4e2*


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
