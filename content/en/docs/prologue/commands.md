---
title: "Commands"
description: "Doks comes with commands for common tasks."
lead: "Doks comes with commands for common tasks."
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu:
  docs:
    parent: "prologue"
weight: 2
toc: true
---

{{< alert icon="💡" text="You can change the commands in the scripts section of `./package.json`." />}}

## create

Create new content for your site:

```bash
npm run create [path] [flags]
```

See also the Hugo docs: [hugo new](https://gohugo.io/commands/hugo_new/).

### Docs based tree

Create a docs based tree — with a single command:

```bash
npm run create -- --kind docs [section]
```

For example, create a docs based tree named guides:

```bash
npm run create -- --kind docs guides
```

## lint

Check scripts, styles, and markdown for errors:

```bash
npm run lint
```

### scripts

Check scripts for errors:

```bash
npm run lint:scripts [-- --fix]
```

### styles

Check styles for errors:

```bash
npm run lint:styles [-- --fix]
```

### markdown

Check markdown for errors:

```bash
npm run lint:markdown [-- --fix]
```

## clean

Delete temporary directories:

```bash
npm run clean
```

## start

Start local development server:

```bash
npm run start
```

## build

Build production website:

```bash
npm run build
```

### functions

Build Lambda functions:

```bash
npm run build:functions
```

### preview

Build production website including draft and future content:

```bash
npm run build:preview
```

<details>
  <summary>Example Request - Auth 200</summary>
  
  ```bash
  curl --location 'https://localhost:7278/api/identity/apps/v1/Auth' \
  --data '{
    "clientId": "roaa_osos_external_system",
    "clientSecret": "EHMcQfTjWnZr4u7ADFJaNdRgUkXp2s5v8yBEHKbPeShVmYq3t6wZH3B4M9"
  }'
</details>
<details>
  <summary>Example Response</summary>
json
Copy code
{
  "data": {
    "info": {
      "rosasClient": {
        "name": "roaa",
        "title": "Roaa Tech"
      },
      "rosasProduct": {
        "name": "osos",
        "title": "OSOS System"
      }
    },
    "token": {
      "accessToken": "eyJhbGciOiJSUzI1NiIsImtpZCI6IjAwRDEzRTlBRUU0NUZBMzY3QkZBMjBDODA0OTI2RDFBIiwidHlwIjoiYXQrand0In0.eyJuYmYiOjE2OTE5MzQ1NDksImV4cCI6MTY5MTkzODE0OCwiaXNzIjoiaHR0cDovL2Rldi5yb3Nhcy5yb2FhLnRlY2giLCJqdGkiOiI5QzI3QzMxQ0Q0Nzc0NkI5OEUzQTZGMzUzRUEzODhFMSIsImlhdCI6IjE2OTE5MzQ1NDkiLCJjbGllbnRfaWQiOiJyb2FhX29zb3NfZXh0ZXJuYWxfc3lzdGVtIiwicGlkIjoiODhlNjczMjgtM2IyMC00MTNlLWI2ZTEtMDEwYjQ4ZmE3YmM5IiwiYW10aCI6ImNsaWVudF9jcmVkZW50aWFscyIsInR5cGUiOiJleHRlcm5hbF9zeXN0ZW0iLCJhdWQiOiJyb3Nhc19hcGlfcmVzb3VyY2UiLCJzY29wZSI6WyJleHRlcm5hbF9zeXN0ZW1fc2NvcGUiXX0.PLHEXXs1t_VbfAc9ykGwAXDnBpN59ekKkKMhxQFfjsTKVfieclSBbohJ1ZFsli8qt48Bdbhxuf6fpf3ghOEkCPOzqsDmCMz9FF_IowGeWo65UP5KiQCpC1-3qai6uw1W5NirEPmRieslYVLpyL4wzighBF6BT3Z58XGlio99vP83d5qt-KvxJTq_RXUIx70SwhTr6MQ7YJ1vKzAqVD8aj4bNEjvAu54P2VQLYqczvg8IzwDnELec7ZCKd4zeGrbxEeQn6gA4qiYE_9qqbVXzmvBPJuH8fvgs5_PSFp4jfQeHp8d1Oy09YvdIaNbLqn4XrkD7l8e9r_VlfCzGECXIvQ"
    }
  },
  "metadata": {
    "errors": [],
    "success": true
  }
}
</details>
```
