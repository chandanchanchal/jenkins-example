pipeline {
    def job_name='$JOB_NAME'
    String[] arr=job_name.split('/');
    
    agent {label '${arr[1]}'}

    stages {
        stage ('Compile Stage') {

            steps {
                  sh 'echo $JOB_NAME'
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
