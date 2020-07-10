### Sanibonani 👋🏾  [?](https://en.wiktionary.org/wiki/sanibonani)

Hi, I'm Qawelesizwe Mlilo(or just Q), a South African based Software Developer. I write code for fun and profit.

Checkout [ping-monitor](https://github.com/qawemlilo/ping-monitor), my uptime event emitter.


#### Installation 

```
npm install ping-monitor
```

#### How to use 

```javascript
const UptimeMonitor = require('ping-monitor');

const monitor = new UptimeMonitor({
    website: 'http://github.com',
    interval: 10 // minutes
});


monitor.on('up', function (res, state) {
  console.log('%s is up', state.website);
});

monitor.on('down', function (res, state) {
  console.log('%s is down', state.website);
});

monitor.on('timeout', function (error, state) {
  console.log('%s timed out', state.website);
});

monitor.on('error', function (error, state) {
  console.error(error);
});
```

