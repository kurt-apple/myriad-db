# Dynamic Schema
One goal of myriad-db is to offer a tool to search for data that matches a certain shape as efficiently as possible. Enclosed are my notes on how this could be achieved.
- Record { id, shapeid, json }
- Shape { id }
- Column { id, title, type }
- ShapeColumn { shapeid, columnid, required }
- App { id, title }
- AppShape { appid, shapeid }
Then, querying for shape would be to scoop up all the shapes with their related columns, and sort through to see what matches the query.
Inserting a record would require validating against its declared shape

If there is an app that uses a shape, but there are additional shapes who require certain other columns, then 
