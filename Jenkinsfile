pipeline{
    agent any 
    stages {
        stage('Build'){
            steps{
                sh 'g++ PES2UG20CS286.cpp -o PES2UG20CS286_exec'
            }
        }

        stage('Test'){
            steps{
                sh '/var/jenkins_home/workspace/PES2UG20CS286/PES2UG20CS286_exec'
                echo 'test successful'
            }
        }

        stage('Deploy'){
            steps{
                echo 'deployed'
            }
        }
        
    }

    post{
        failure{
            echo 'pipeline failed'
        }
    }
}
