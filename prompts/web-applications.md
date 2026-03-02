## Analyze Daemons

```
Enumerate, analyse, and describe the asynchronous BloodHound daemons (workers). Include a summary of their functionality, their trigger (time-based, messing queue, database entries), their inputs (highlight any inputs we can tamper with), and their source code locations.
```

## Web API Request Handler

```
Show me the code path for Cypher queries submitted to the POST /api/v2/graphs/cypher. The following is the request body for context: {"query":"MATCH p = (t:Group)<-[:MemberOf*1..]-(a)\nWHERE (a:User or a:Computer) and t.objectid ENDS WITH '-512'\nRETURN p\nLIMIT 1000","include_properties":true}'
```