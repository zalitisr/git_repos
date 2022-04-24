## Salīdzināt vienādu failu (ne README) hash no mapes module_1 un module_2. Vai git redz atšķirību starp šiem failiem?
> git ls-files -s
160000 c4b75e99c2ac1830a7905c5ec73f34c9ac194923 0       first
100644 a38cd4f81506904fc8cb9c2249c718682a0c78ca 0       module_1/HelloWorld.png
100644 db4f66f255ce2c26cd51018aec0979eb9db4511f 0       module_1/HelloWorld.py
100644 e7d844cb91ab22153cfc014ebf18441adf4997fa 0       "module_1/LU_7.k._DevOps_pamati_ies\304\201c\304\223jiem_M\304\201jasdarbs_01. lekcijas uzdevumi (2).pdf"
100644 115fa575dea1b8a7e351a874d1e3e15b03403d92 0       module_1/git.png
100644 da206fd3d525918f9a5cfc50b4346dde32a3eaa2 0       module_1/readme.md
100644 a38cd4f81506904fc8cb9c2249c718682a0c78ca 0       module_2/HelloWorld.png
100644 db4f66f255ce2c26cd51018aec0979eb9db4511f 0       module_2/HelloWorld.py
100644 e7d844cb91ab22153cfc014ebf18441adf4997fa 0       "module_2/LU_7.k._DevOps_pamati_ies\304\201c\304\223jiem_M\304\201jasdarbs_01. lekcijas uzdevumi (2).pdf"
100644 115fa575dea1b8a7e351a874d1e3e15b03403d92 0       module_2/git.png
100644 f0ba86cc65a24a036ad13f05a1b79f746a62e8e9 0       module_2/readme.md

## Pārbaudīt kādas izmaiņas tika veiktas iepriekšējās nedēļas laikā. Atrast vismaz divus veidus kā to izdarīt.
> git log --pretty=format: --name-only --since="7 days ago" | sort | uniq
> git log --after='2017-07-01 00:00:00' 

## Atrast commit kurus veica autors - “Laura Pacilio”
> git log --author="Laura Pacilio"

## Atrast vai Laura ir veikusi commit pagājušā gada septembrī?
> git log --since='Sep 1 2021' --until='Sep 30 2021' --author="Laura Pacilio"

# Vai Laura ir veikusi commit vakar?
> git log --since=yesterday.midnight --author="Laura Pacilio"

```sh
Autors: Ritvars Zālītis
```