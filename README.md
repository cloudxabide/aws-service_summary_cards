# AWS Service Summary Cards

STATUS: pre-beta testing some stuff

I *think* asciidoc might be a good way to approach this.  Github markdown is not universal, but maybe universal enough?

## Format
```
(ServiceName)/What  
             /Who  
             /Where  
             /When  
             /Why  
```
 
## Create new Service Summary Directory

```
SERVICE_NAME="EC2"
mkdir -p ${SERVICE_NAME}/

for FILE in What Who Where When Why;
do 
  [ ! -f ${SERVICE_NAME}/${FILE}.adoc ] && { echo "= $FILE" > ${SERVICE_NAME}/${FILE}.adoc; }
done
[ ! -f ${SERVICE_NAME}/main.adoc ] && { 
echo "= $SERVICE_NAME" > ${SERVICE_NAME}/main.adoc
for FILE in What Who Where When Why;
do 
  echo ""
  echo "include::$FILE.adoc[]  " >> ${SERVICE_NAME}/main.adoc
done
}

```
