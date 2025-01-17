# Commands

## Status

This command give a basic status of the elasticsearch cluster and for the different storage services:

```
ems:status
```

This command has 3 option:

 - `--silent`: if turned on the command only shows errors and warnings
 - `--wait-for-status=green`: the command will wait that the elasticsearch status is green (useful when you chain commands)
 - `--timeout=30s`: If no response form the elasticsearch cluster after the timeout and the status will be considered as red

## Curl

This command allows you to save request to a file. Usage: 

```
ems:curl /public/view/54 /opt/samples/test.pdf --save --base-url=http://demo-admin-dev.localhost
```

In this example the request `/public/view/54` will be saved to the file `/opt/samples/test.pdf`. With the `--save` option the file will be uploaded to the storages services. And the `--base-url=http://demo-admin-dev.localhost` option will generate an url to the user. Is the `base-url` option is defined the file will be saved even if the `--save` is not specified.   