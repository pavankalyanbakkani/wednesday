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
                echo 'Bridgewater, Newjersey'
                
            }
        }
        stage('Descr') {
            steps {
                echo 'Hyuderabad'
                echo 'Suncity'
               
            }
        }
    }

    post {
        success {
            echo "Finally"
       
         }
   failure { // This post condition will run if any of the stages fail
            echo 'The build has failed!'
            // You can add more steps or calls here to record the failure in other tools or send notifications.
        }
    }
}
