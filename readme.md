
## Server logging for web apps

![Area chart](https://img.icons8.com/ios/250/eeeeee/area-chart.png)

<!-- #### [Meetup XXX](https://www.meetup.com/XXX) -->
<!-- npm install; npm start -->

###### [TheodorosPloumis.com](http://www.theodorosploumis.com/en) / [@theoploumis](http://twitter.com/theoploumis)
________________________

###### Get them: [online presentation](http://theodorosploumis.github.io/logging-presentation) / [source code](https://github.com/theodorosploumis/logging-presentation)

###### Under [Attribution 4.0 International](http://creativecommons.org/licenses/by/4.0/) license. Icons by [icons8](https://icons8.com).

---

### What is this talk about

- What is logging
- Why we need logging
- Common logging formats
- Logging examples
- Logging tools

---

### What is logging

![Domain click](https://png.icons8.com/carbon-copy/150/eeeeee/domain.png)

---

### Why we need logging
- Protect our app
- Know what is going on
- Know our visitors
- Plan our resources & needs
- Data is Data

![Protection](https://img.icons8.com/ios/150/eeeeee/hips.png)

---

### How it works

![Server logging diagram](images/logging-diagram.png)

---

### Log format variables
```
<1. IP/domain> <2. user> <3. datetime> <4. request> <5. http-status> \
<6. request-size> <7. referrer> <8. user-agent> <9. request-time>

IP: 62.109.16.162
user: -
datetime: [26/Feb/2019:00:11:13 +0200]
request: "GET /index.php HTTP/1.1"
http-status: 200
request-size: 20702
referrer: "/user/login"
user-agent: "Mozilla/5.0 ... Chrome/43.2357.125 Safari/537.36"
request-time: 0.4
```

![Log formats](https://img.icons8.com/ios/150/eeeeee/log.png)

---

### Common log formats
```
// Common Log Format (CLF)
"%h %l %u %t \"%r\" %>s %b"

// Common Log Format with Virtual Host
"%v %h %l %u %t \"%r\" %>s %b"

// Extended/combined log format
"%h %l %u %t \"%r\" %>s %b \"%{Referer}i\" \"%{User-agent}i\""

// Referer log format
"%{Referer}i -> %U"

// Agent (Browser) log format
"%{User-agent}i"
```

See [apache log formats](https://httpd.apache.org/docs/2.4/mod/mod_log_config.html).

---

### Logging examples

- [Real logs](#)

---

### Open source logging tools

- [rsyslog](https://www.rsyslog.com)
- [graylog](https://www.graylog.org)
- [logwatch](https://sourceforge.net/projects/logwatch)/[ELK stack](https://www.elastic.co/elk-stack)
- [logstash](https://github.com/elastic/logstash)
- [fluentd](https://www.fluentd.org)
- ... many non open-source tools

![Case](https://img.icons8.com/ios/150/eeeeee/toolbox.png)

---

### Tips

- include a timestamp
- format in JSON
- don't log insignificant events
- log all application errors
- write messages in a human-readable form
- don't log informational data in production
- don't log anything a human can't read or react to
- if you save logs use a nosql database

---

### Demo

- [demo](#)

---

### Thank you!

Join [Serres Hackathon 2019](http://hackathon.serrestech.gr) 11 & 12 May 2019

#### Questions?
