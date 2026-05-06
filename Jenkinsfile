pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo 'Building...'
            }
        }
        post{
            success{
                mail to: "huynhkimtuyen203@gmail.com",
                subject: "Build Status Email",
                body: "The build was successful. Please check the Jenkins console for details."
                
            }
        }
    }
}