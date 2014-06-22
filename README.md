# node-visualdns-ddns

Dynamic DNS register for [VisualDNS.net](https://visualdns.net)

It was specifically implemented in order to update the A entries based on the current Internet public IP.
Ideally for home servers

## Installation

You must have previously installed [node.js](https://nodejs.org) 

```bash
$ npm install -g visualdns-ddns
```

## Usage

Create the config file
```json
{
  "token": "<VisualDNS API token>",
  "domains": [
    { "name": "mydomain.net", "type": "A", "TTL": 3600 }
  ]
}
```

Usage
```
$ vddns -c config.json
```

Scheudle it in crontab every 15 minutes
```bash
*/15 * * * * vvdns -c /etc/vddns/config.json
```

## License

[MIT](http://opensource.org/licenses/MIT) © Tomas Aparicio
