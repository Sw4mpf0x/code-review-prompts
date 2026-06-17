## Analyze Daemons

```
Enumerate, analyse, and describe the asynchronous BloodHound daemons (workers). Include a summary of their functionality, their trigger (time-based, messing queue, database entries), their inputs (highlight any inputs we can tamper with), and their source code locations.
```

## Web API Request Handler

```
Show me the code path for Cypher queries submitted to the POST /api/v2/graphs/cypher. The following is the request body for context: {"query":"MATCH p = (t:Group)<-[:MemberOf*1..]-(a)\nWHERE (a:User or a:Computer) and t.objectid ENDS WITH '-512'\nRETURN p\nLIMIT 1000","include_properties":true}'
```

## Obtain a overview of the structure of a web application

```
Analyze the source code of the application. Generate a markdown file named "overview.md" with these sections "description", "authentication", "authorization model", "web entry points", "security features". For the section "description" you will describe the purpose of the application. For the section "authentication" you will specify in which files authentication is defined and enforced. For the section "authorization model" you will specify in which files authorization rules are defined and enforced. For the section "web entry points" you will specify all the endpoints exposed by the application and in which files they are defined. For the section "security features" you will specify each features that perform processing like ciphering, hashing, random content generation, digital signature and in which files they are defined.
```
