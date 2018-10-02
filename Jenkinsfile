node {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven 3.0.5') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven 3.0.5') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven 3.0.5') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
