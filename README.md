### Sanibonani 👋🏾  [?](https://en.wiktionary.org/wiki/sanibonani)

Hi, I'm Qawelesizwe Mlilo(or just Q), a South African based Software Developer. I write code for fun and profit.



<table style="border: none;vertical-align:top;">
<tr style="border: none;">
<td style="border: none;" width="50%">
Checkout [ping-monitor](https://github.com/qawemlilo/ping-monitor), an uptime event emitter that I use to monitor my websites and APIs.


#### Installation 

```
npm install ping-monitor
```

#### How to use 

```javascript
const UptimeMonitor = require('ping-monitor');

const monitor = new UptimeMonitor({
    address: 'https://github.com',
    protocol: 'http',
    interval: 10,
    config: {
      intervalUnits: 'minutes'
    },
    expect: {
      statusCode: 200
    }
});


monitor.on('up', function (res, state) {
  console.log('%s is up', state.address);
});

monitor.on('down', function (res, state) {
  console.log('%s is down', state.address);
});

monitor.on('restored', function (res, state) {
  console.log('%s has been restored', state.address);
});

monitor.on('timeout', function (error, state) {
  console.log('%s timed out', state.address);
});

monitor.on('error', function (error, state) {
  console.error(error);
});
```
</td>

<td style="border:none;vertical-align:top;" width="40%">


### Recent Blog Posts


* [Auto-registering events and listeners in Laravel 5.8](https://blog.ragingflame.co.za/2019/10/23/autoregistering-events-and-listeners-in-laravel-58)
* [Building a twitter bot for posting the latest package releases on Github](https://blog.ragingflame.co.za/2018/3/19/building-a-twitter-bot-for-posting-the-latest-package-releases-on-github)
* [Handling Node.js migrations with knex and widget-knex-schema](https://blog.ragingflame.co.za/2016/10/3/handing-nodejs-migrations-with-knex-and-widgetknexschema)
</td>
</tr>
</table>

