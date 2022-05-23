
# getStudyURL
Implementación para Clinica del Pilar
>*Metodo que recibe el DNI + AN y devuelve la url del estudio*


**Metodo:** *GET*


**URL:** *[https://pacs.clinicadelpilartuc.com.ar/api/study/getstudyurl.php](https://pacs.clinicadelpilartuc.com.ar/api/study/getstudyurl.php)*


**Authorization Token:** *871b2cd8-6018-46ed-9490-f86ec77fa4e2*


**Parametros:** 
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
- **401 Unauthorized token** - - Response Schema: application/json
```markdown
   resultError: object	
	message: string
```
