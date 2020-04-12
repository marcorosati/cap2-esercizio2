SETUP
pull image registry.access.redhat.com/rhscl/nodejs-6-rhel7
TASK
deploy app in https://github.com/marcorosati/app-config.git 
-builder image rhscl/nodejs-6-rhel7
-project ->app-config
-appname-> myapp
-npm_config_registry=npm registry->https://registry.npmjs.org
-myappconf APP_MSG="text message"
-myappsec in home/student/app/config myappfilesec

myappconf as env
myappsec as volume
