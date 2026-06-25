pipeline {
    // Tells Jenkins to run this on your specific agent
    agent { label "Jenkins-Agent" }

    // We don't need the 'tools' block right now because we aren't using Java or Maven!

    stages {
        stage("Verify Checkout") {
            steps {
                // Jenkins automatically downloaded your repo before this started.
                // 'ls -la' will list the files so you can see your README and Jenkinsfile in the Jenkins console!
                sh "echo 'Checking what files are in the workspace:'"
                sh "ls -la" 
            }
        }

        stage("Simulate Build Application"){
            steps {
                // We are just printing text to the console to pretend we are building
                sh "echo 'Pretending to compile code...'"
                sleep 2 // Pauses for 2 seconds just for visual effect
                sh "echo 'Build successful!'"
            }
        }

        stage("Simulate Test Application"){
            steps {
                sh "echo 'Running fake tests...'"
                sleep 2
                sh "echo '10/10 Tests Passed!'"
            }
        }
    }  
    
    // Cleans up the workspace after the pipeline finishes
    post {
        always {
            cleanWs()
        }
    } 
}
