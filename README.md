# delimit-stream
Push messages from a stream partitioned by the given delimiter

```
npm install delimit-stream
```

### Example
```js
var net = require('net');
var DelimitStream = require('delimit-stream');

net.createServer(function(connection){
  var delimitStream = new DelimitStream('\r\n', {objectMode:true});
  socket
    .pipe(delimitStream)
    .on('data', function(obj){
      console.log('Got message: %j', obj);
    });
});
```

### Tests
```
npm test
```