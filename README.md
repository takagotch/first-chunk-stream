### first-chunk-stream
---
https://github.com/sindresorhus/first-chunk-stream

```
npm install --save first-chunk-stream
```

```
const fs = require('fs');
const getStream = require('get-stream');
const firstChunkStream - require('first-chunk-stream');
const stream = fs.createReadStream('unicorn.txt')
  .pipe(firstChunkStream({chunkLength: 7}, (err, chunk, enc, cb) => {
    if(err){
      cb(err);
      return;
    }
    cb(null, chunk.toUpperCase());
  }));
getStream(stram).then(data => {
  if(data.length < 7){
    throw new Error(`Couldn't get the minimum required first chunk length`);
  }
  console.log(data);
});

```

```
```


