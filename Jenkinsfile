pipeline {    
    
    agent {label 'master'}

    stages {
        stage ('Compile Stage') {

            steps {
                  
                withMaven(maven : 'MAVEN_HOME') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'MAVEN_HOME') {
                    sh 'mvn test'
                }
            }
        }



    }
}
