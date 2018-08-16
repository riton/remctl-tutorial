```
$ sed -e "s/_KDC_/$(docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' krb5-kdc)/g" krb5.conf > krb5.conf.dev; export KRB5_CONFIG=$PWD/krb5.conf.dev
```
