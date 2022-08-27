# AWS Service Summary Cards

STATUS: pre-beta testing some stuff

I *think* asciidoc might be a good way to approach this.  Github markdown is not universal, but maybe universal enough?

## Format
<ServiceName>/What
             /Who
             /Where
             /When
             /Why
 
## 
SERVICE_NAME="EC2"
mkdir -p ${SERVICE_NAME}/{What,Who,Where,When,Why}.adoc
[ ! -f ${SERVICE_NAME}/main.adoc ] && { echo "# $SERVICE_NAME" > ${SERVICE_NAME}/main.adoc; }
