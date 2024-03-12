Each .csv file is used in Azure Data Factory.

# Activities

## Copy Data
- **Name:** xxx

# Source
- **Source:** HTTP
  - **Format:** CSV
    - **Name:** xxxHTTP
      - **Base URL:** https://raw.githubusercontent.com/user/folder/main/xxx.csv
      - **Authentication Type:** Anonymous
  - **First Row as Header:** true
  - **Import Schema:** none

# Sink
- **Azure Data Lake Storage Gen2**
  - **Name:** xxxSink
    - **Service:** yourservice
    - **File Path:** path/to-your/xxx.csv
  - **First Row as Header:** true
  - **Import Schema:** none

## Athletes example

```
{
    "name": "data-ingestion",
    "properties": {
        "activities": [
            {
                "name": "Athletes",
                "type": "Copy",
                "dependsOn": [],
                "policy": {
                    "timeout": "0.12:00:00",
                    "retry": 0,
                    "retryIntervalInSeconds": 30,
                    "secureOutput": false,
                    "secureInput": false
                },
                "userProperties": [],
                "typeProperties": {
                    "source": {
                        "type": "DelimitedTextSource",
                        "storeSettings": {
                            "type": "HttpReadSettings",
                            "requestMethod": "GET"
                        },
                        "formatSettings": {
                            "type": "DelimitedTextReadSettings"
                        }
                    },
                    "sink": {
                        "type": "DelimitedTextSink",
                        "storeSettings": {
                            "type": "AzureBlobFSWriteSettings"
                        },
                        "formatSettings": {
                            "type": "DelimitedTextWriteSettings",
                            "quoteAllText": true,
                            "fileExtension": ".txt"
                        }
                    },
                    "enableStaging": false,
                    "translator": {
                        "type": "TabularTranslator",
                        "typeConversion": true,
                        "typeConversionSettings": {
                            "allowDataTruncation": true,
                            "treatBooleanAsNumber": false
                        }
                    }
                },
                "inputs": [
                    {
                        "referenceName": "Athletes",
                        "type": "DatasetReference"
                    }
                ],
                "outputs": [
                    {
                        "referenceName": "ADLS",
                        "type": "DatasetReference"
                    }
                ]
            }
        ]
    }
}
```

Validate
Debug

after that raw-data is completed
![raw-data-files](/img/data.PNG)

