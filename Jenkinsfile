pipeline {
    agent {label 'feature'}

    stages {
        stage ('Compile Stage') {

            steps {
                echo 'Hello from develop once more'
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
