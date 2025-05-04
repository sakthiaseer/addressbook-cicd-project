pipeline{
    agent any
    stages{
        stage("checkout code from github"){
         steps{
          echo "git checkout starting"
          git url:"https://github.com/sakthiaseer/addressbook-cicd-project/" 
          echo "git checkout done"
         }
        }
        stage("compile the project"){
            steps{
                echo "compiling started"
                sh "mvn compile"
            }
        }
         stage("stage4: package"){
            steps{
                sh "mvn package"
            }
        }
stage("deploy the project"){
         steps{
             sh "sudo cp /var/lib/jenkins/workspace/testpipeline/target/addressbook.war /home/ubuntu/apache-tomcat-9.0.104/webapps"
         }
        }

}
}
