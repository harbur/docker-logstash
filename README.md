docker-logstash
===============

docker logstash configuration

This is based on digitalwonderland/logstash and adds support for json parsing of input files.

To use this, add on your docker image a file `/etc/logstash-forwarder.conf` with the following content:

```
{
  "files": [
    {
      "paths": [
        "/full/path/to/the/logfile.log"
      ],
      "fields": { "type": "json", "app": "myappname" }
    }
  ]
}
```
