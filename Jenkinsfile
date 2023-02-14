pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -c main/PES1UG20CS653.cpp'
                sh 'g++ -o PES1UG20CS653 main/PES1UG20CS653.cpp'
                echo 'build stage successfull'
            }
        }
        stage('Test'){
            steps{
                sh './PES1UG20CS653'
                echo 'test stage successful'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deployment Successful'
            }
        }
    }
    post{
        failure{
            echo 'Pipeline Failed'
        }
    }
}
