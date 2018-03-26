
A simple paper wallet generator for Ethereum net.

 Run project

    Run

```
npm install
```

    You need to verify public key (make sure that you have gpg installed).
    In order to do it, just run the next code in the console:
```
gpg --verify index.html.sig
```


    Then you will see something like this

```
    gpg: assuming signed data in 'index.html'
     gpg: Signature made Fri Feb 26 08:07:40 2016 EET
     gpg:                using RSA key E3A5CD636B210365
     gpg: Can't check signature: No public key
```

    The next step:
```
gpg --no-default-keyring --keyring vendors.gpg --keyserver pgp.mit.edu --recv-key RSA_key_ID
```

    for previous example it will be
```
gpg --no-default-keyring --keyring vendors.gpg --keyserver pgp.mit.edu --recv-key E3A5CD636B210365
```

    The response will be

```
    gpg: requesting key 9741E8AC from hkp server pgp.mit.edu
     gpg: /home/andrzejl/.gnupg/trustdb.gpg: trustdb created
     gpg: key 9741E8AC: public key “Pierre Schmitz ” imported
     gpg: no ultimately trusted keys found
     gpg: Total number processed: 1
     gpg: imported: 1 (RSA: 1)
```

     Next:

```
   gpg --verify --verbose --keyring vendors.gpg index.html.sig
```


     Run

```
gulp
```

     Open index.html file in the browser


