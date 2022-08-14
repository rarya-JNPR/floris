pipeline {
 
    agent any
    envirinment {
     NEW_VERSION = '1.0'
 }
 parameters {
     choice(name: 'VERSION', choices: ['1.0', '1.1', '1.2'], description: '')
     choice(name: 'exectest', defaultvalue: true, description: '')
 }
    stages {
    
       stage("Build") {
         
          steps {
             echo "Building this Application"
             echo "Building version is ${NEW_VERSION}"
          }
        }
       stage("Testing") {
        when {
         expression {
          params.VERSION == 1.0
            }
        }
          steps {
             echo "Testing this Application"
          }
        }
       stage("Deploy") {
         
          steps {
             echo "Deploying this Application"
             echo "Deployed version is ${NEW_VERSION}"
          }
        }
      }
   }
