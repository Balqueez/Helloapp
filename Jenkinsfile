Pipeline{
      agent any

   stages{
        stage('checkout'){
             steps{
                 git 'https://your-git-repo-url.git'
                 }

        }
        stage('Build Docker Image')
        {
            steps{
                script{
                    dockerImage=docker.build("hello-node-app:${env.BUILD_ID}")
                }

            }
        }

        stage('Run Container')
        {
           steps{
                script {
                    docker.image("hello-node-app:${env.BUILD_ID}").run('-p 3000:3000')
           

                }
            }
        }

    }
     post {
        always {
            cleanWs()
        }
    }
}