
```markdown

**Metodo:** GET

[**URL:**](https://pacs.clinicadelpilartuc.com.ar/api/study/getstudyurl.php)

**Authorization Token:** *871b2cd8-6018-46ed-9490-f86ec77fa4e2*

**Parametros:** 
- pat_id - integer
- accession_no - integer

**Responses:**
200 OK - Response Schema: application/json

  result: Array of objects
  	Array [
   	  url: string
        ]
	
200 OK	- Response Schema: application/json

   result: object	
	message: string
	
400 Bad Request - Response Schema: application/json

   resultError: object	
	message: string

401 Unauthorized token

   resultError: object	
	message: string
```




## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/PentalogicTech/pentalogictech.github.io/edit/main/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/PentalogicTech/pentalogictech.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
