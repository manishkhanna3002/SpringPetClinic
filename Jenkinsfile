pipeline {
    agent{label "master"}
    tools{maven "m3"}
    stages {
        stage ("Checkout") {
            steps {
                git branch: "main'", url: "https://github.com/manishkhanna3002/SpringPetClinic.git"
            }
        }
        stage("Build") {
            steps {
                sh "mvn: compile"
            }
        }
        stage("Test") {
            steps {
                sh "mvn: test"
            }
        }
        stage("Package") {
            steps {
                sh "new package"
            }
        }
        stage("Deploy") {
            steps {
                sh "java -jar /var/lib/jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar"
            }
        }
    }
}
