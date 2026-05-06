pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo 'Build the code using a build automation tool to compile and package your code.'
                echo 'Tool: Maven, mvn clean compile package'
            }
        }
        stage('Unit and Integration Tests'){
            steps{
                echo 'Run unit tests to ensure the code functions as expected and run integration tests to ensure the different components of the application work together as expected.'
                echo 'Tool: OWASP Dependency Check or Synk'
            }
        }
        stage('Code Analysis'){
            steps{
                echo 'Integrate a code analysis tool to analyse the code and ensure it meets industry standards.'
                echo 'Tool: SonarQube (integrated with Jenkins)'
            }
        }
        stage('Security Scan'){
            steps{
                echo 'Perform a security scan on the code using a tool to identify any vulnerabilities. Research and select a tool to scan your code.'
                echo 'Tool: OWASP Dependency Check or Snyk'
            }
        }
        stage('Deploy to Staging'){
            steps{
                echo 'Deploy the application to a staging serverdation.'
                echo 'Tool: AWS CLI / scp to EC2 instance'
            }
        }
        stage('Integration Tests on Staging'){
            steps{
                echo 'Run integration tests on the staging environment to ensure the application functions as expected in a production-like environment.'
                echo 'Tool: Postman/Newman or Selenium'
            }
        }
        stage('Deploy to Production'){
            steps{
                echo 'Deploy the application to a production server'
                echo 'Tool: AWS CodeDeploy or Ansible'
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