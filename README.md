
Open the terminal in this directory and run:

```
$ docker-compose up -d
```


## Test functionality through IRIS terminal
Run the below command to start IRIS terminal from VS CODE terminal
```
$ docker-compose exec iris iris session iris
```


### View existing data 
Run the below command in IRIS terminal to view the existing data
```
do ##class(dc.VectorLab.Base).ListData()
```

### Inserting vector data
Run the below command to insert vector data
```
do ##class(dc.VectorLab.Base).SaveData("Input data testing")
```

### View vector data
Run the below command to view vector data in IRIS terminal and pass the ID
```
set vector =  ##class(dc.VectorLab.Base).ViewData(8,2) 
write vector
```

### Performing Vector Search
Run the below command to search vector data
```
set vector =  ##class(dc.VectorLab.Base).VectorSearch("The fox and the chicken")
```

### HuggingFace Text generation using GPT2 LLM
Run the below command by passing some text, application will generate the text accordingly to search vector data
```
set test=##class(dc.VectorLab.Base).Generate("Generative AI is")
write test
```
### HuggingFace Text generation using HuggingFace Endpoint

```
Set test = ##class(dc.VectorLab.Base).GenerateHF("what is machine learning?")
write test
```



