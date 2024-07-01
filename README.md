# extract-pdf
### 1. Run `docker compose up` to start ES and Kibana
### 2. Run script in main.ipynb to extract data from PDF file and put it to ES
### 3. Open Kibana client to query: http://localhost:5601/app/dev_tools#/console
Query like that:
```
GET  /s3_guide/_search
{
  "query": {
    "match": {
      "content": "EventBridge event message structure"
    }
  }
}

```
