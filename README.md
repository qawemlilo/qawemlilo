### Sanibonani 👋🏾  [?](https://en.wiktionary.org/wiki/sanibonani)

Hi, I'm Qawelesizwe Mlilo(or just Q), a South African based Software Developer. I write code for fun and profit.

Checkout [ping-monitor](https://github.com/qawemlilo/ping-monitor), an uptime event emitter that I use to monitor my websites and APIs.


#### Installation 

```
npm install ping-monitor
```

#### How to use 

```javascript
const UptimeMonitor = require('ping-monitor');

const monitor = new UptimeMonitor({
    website: 'http://github.com',
    interval: 10,
    config: {
      intervalUnits: 'minutes'
    },
    expect: {
      statusCode: 200
    }
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

