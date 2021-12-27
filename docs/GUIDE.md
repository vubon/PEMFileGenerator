For Generating PEM file follow below steps

1. Generate PEM file 
```python
from PEMFileGenerator.ssh_pem import Generate

# Password login disable
gen = Generate(ip="192.168.56.15", user="vagrant", password="vagrant")
try:
    gen.run()
except Exception as err:
    print(err)
```
2. You will get 192-168-56-15.pem like this one. Now change mod of the file
```shell
sudo chmod 400 192-168-56-15.pem
```
3. Now access your server by using 192-168-56-15.pem file 
```shell
ssh -i 192-168-56-15.pem vagrant@192.168.56.15
```
4. Well done. 

[N.B. 192.168.56.15 this is a sample IP address and as well user and password]