

# Public Key Infrastructure Assignment
 
For this assignment, you will be using OpenSSL.
If you are using Windows, you will have to download the free application [Cygwin](https://www.cygwin.com), which provide functionality similar to a Linux distribution on Windows.
If you use Linux or MacOS, you just have to run the terminal application.

## Encryption
Within the terminal type `touch original.txt` to create an empty file. Type then `echo Industrial IoT is interesting > original.txt`  to insert the text *Industrial IoT is interesting* into the file.
If you want to see what is in the original.txt file, type ```cat original.txt```
To encode the file original.txt, you can use

```
$ openssl enc -base64 -in original.txt -out encoded.txt
```

To decode a file the decrypt option (-d) has to be used

```
$ openssl enc -d -base64 -in text.base64 -out text.plain
```

Generate CA files serverca.crt and servercakey.pem. This allows the signing of server and client keys:
$ openssl genrsa -out servercakey.pem
$ openssl req -new -x509 -key servercakey.pem -out serverca.crt

#kul4 #pki