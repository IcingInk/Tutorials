For code explanation and additional configurations read the tutorial at https://javatutorial.net/java-file-upload-rest-service 


# deployed

1. deployed in Tomcat version 8.0.27
2. upload file -> http://localhost:8080/FileUploader/fileuploader.html 
3. after a successful uploading http://localhost:8080/FileUploader/rest/upload 

Upgraded the version of Jersey to 1.19.4
1. The restful-services are defined in the file FileUploadService.java
2. hardcoded : the 'UPLOAD_FOLDER' to point at 
2. The name of the war-file is set in the pom.xml -> ```<finalName>FileUploader</finalName>```


# Creating a large file,  uploading the file using firefox.

## 2G

```
#!/bin/bash
fallocate -l 2G gentoo_root.img
```

**file before:**
1. source-dir> md5sum gentoo_root.img
2. a981130cf2b7e09f4686dc273cf7187e  gentoo_root.img

**file after:**
1. target-dir> md5sum gentoo_root.img
2. a981130cf2b7e09f4686dc273cf7187e  gentoo_root.img

**works**

## 3G

```
#!/bin/bash
fallocate -l 3G gentoo_3.img
```

**file before:**
1. source-dir> md5sum gentoo_3.img
2. c698c87fb53058d493492b61f4c74189  gentoo_3.img

**file after:**
1. target-dir> md5sum gentoo_2.img
2. c698c87fb53058d493492b61f4c74189  gentoo_3.img

**works**

## 4G

```
#!/bin/bash
fallocate -l 4G gentoo_4.img
```

**file before:**
1. source-dir> md5sum gentoo_4.img
2. c9a5a6878d97b48cc965c1e41859f034  gentoo_4.img

**file after:**
1. target-dir> md5sum gentoo_4.img
2. c9a5a6878d97b48cc965c1e41859f034  gentoo_4.img

**works**


## 5G

```
#!/bin/bash
fallocate -l 5G gentoo_5.img
```

**file before:**
1. source-dir> md5sum gentoo_5.img
2. ec4bcc8776ea04479b786e063a9ace45  gentoo_5.img

**file after:**
1. target-dir> md5sum gentoo_5.img
2. ec4bcc8776ea04479b786e063a9ace45  gentoo_5.img

**works**


## 6G

```
#!/bin/bash
fallocate -l 6G gentoo_6.img
```

**file before:**
1. source-dir> md5sum gentoo_6.img
2. 58cf638a733f919007b4287cf5396d0c  gentoo_6.img

**file after:**
1. target-dir> md5sum gentoo_6.img
2. 58cf638a733f919007b4287cf5396d0c  gentoo_6.img

# Fetching information from files.

1. Using the Apache Tika project -> https://tika.apache.org/ 
2. maven artifacts here -> https://mvnrepository.com/artifact/org.apache.tika/tika-parsers

## Image (png, jpeg, jpg)

## PDF


## ZIP


