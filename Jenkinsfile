pipeline {
    agent {
        node {
            label 'built-in' // Use Jenkins' built-in node
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Pavan kalyan bakkani'
                echo 'Bridgewer, Newjersey'
            }
        }
        stage('Descr') {
            steps {
                echo 'Hyuderabad'
                echo 'Suncityy'
            }
        }
    }

    post {
        success {
            script {
                withCredentials([string(credentialsId: 'sleuth', variable: 'SLEUTH_API_KEY')]) {
                    def response = httpRequest(
                        url: 'https://app.sleuth.io/api/1/deployments/testtoken/wednesday-5/register_deploy',
                        httpMode: 'POST',
                        contentType: 'APPLICATION_JSON',
                        headers: [[$class: 'StringParameterValue', name: 'Authorization', value: "Bearer ${SLEUTH_API_KEY}"]],
                        validResponseCodes: '100:599' // this ensures all responses are treated as valid
                    )
                    echo "Response from Sleuth: Status: ${response}"
                }
            }
        }
    }
}
