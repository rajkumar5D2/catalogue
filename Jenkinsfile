// #!groovy
// // it means the libraries will be downloaded and accessible at run time
// @Library('roboshop-shared-library') _

// def configMap = [
//     application: "nodeJSVM",
//     component: "catalogue"
// ]
// env

// // this is .groovy file name and function inside it
// //if not master then trigger pipeline
// if ( ! env.BRANCH_NAME.equalsIgnoreCase('master')){
//     pipelineDecission.decidePipleine(configMap)
// }
// else{
//     echo "master PROD deployment should happen through CR"
// }

pipeline {
    agent { node {label 'agent-1'} } 
    stages {
        stage('Stage 1') {
            steps {
                echo 'Hello world!' 
            }
        }
        stage('unit test') {
            steps {
                echo 'performing unit testing!' 
            }
        }
              //sonar-scanner command expect sonar-project.properties should be available
        stage('Sonar Scan') {
            steps {
                // sh 'ls -ltr'
                sh 'sonar-scanner'
            }
        }
    }
}