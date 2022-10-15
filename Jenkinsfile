pipeline {    
    
    agent {label 'dev'}

    stages {
        stage ('Compile Stage') {

            steps {
                echo 'hello from master1'  
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
