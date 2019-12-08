# Elastic Search Docs

## Linux installation

- wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.5.0-darwin-x86_64.tar.gz
- wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.5.0-darwin-x86_64.tar.gz.sha512
- shasum -a 512 -c elasticsearch-7.5.0-darwin-x86_64.tar.gz.sha512
- tar -xzf elasticsearch-7.5.0-darwin-x86_64.tar.gz
- cd elasticsearch-7.5.0/
- ./bin/elasticsearch

## Commands

- GET
  http:localhost:9020

### To create index(db)

- PUT
  http:localhost:9020/{{db name}}

### To check available index

- GET
  http://localhost:9200/_cat/indices?

### To insert data

- POST  
   http://localhost:9200/movies/movie/
  Data as json

- To give custom id
  http://localhost:9200/movies/movie/{id number}

### To delete data

- DELETE  
  http://localhost:9200/movies/movie/{ID NUMBER}

## Search datas

- To get all data
  http://localhost:9200/movies/_search
- search for query word in all fields of data and return results , even partial word match is returned
  http://localhost:9200/movies/_search?q=Action
- search data using field name
  http://localhost:9200/movies/_search?q=genre:action

## Update new field to schema

- PUT

```
  http://localhost:9200/movies/_mapping
  {
  "properties": {
  "title": { "type": "text"}
  }
  }
```

```
{
  "properties": {
    "title3":   { "properties" : {
            "first" : {
              "type" : "text"
            },
            "last" : {
              "type" : "text"
            }
    }
  }
}
}

```

# Reference link

https://medium.com/@animeshblog/elasticsearch-the-beginners-cookbook-1cf30f98218
