![](https://blog-assets.risingstack.com/2017/09/http-timing-nodejs.png)

### request package也提供了类似功能
```
const request = require('request')

request({
  uri: 'https://risingstack.com',
  method: 'GET',
  time: true
}, (err, resp) => {
  console.log(err || resp.timings)
})
```

### 还有个分布式的 [@risingstack/opentracing-auto](https://github.com/RisingStack/opentracing-auto) 但这个需要和opentracing合着用