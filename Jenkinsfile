node {

   stage('Checkout') {
        // Get code from GitHub repo
        
       
   }
   stage('Build Maven') {
        sh  'cd techkubetest/application'
        sh 'mvn clean install'
		sh 'maven build'
   }
   stage ('build docker image'){
        sh 'cd techkubetest/application'
        sh 'docker build -t techtask .'
   }
   stage ('push Image to Remote repo'){
		sh 'docker push techkubetest:latest'
   }
   stage ('Deploying application to K8 Cluster'){
		sh 'gcloud container clusters get-credentials test-cluster --region us-central1'
        sh 'cd techkubetest/application/deploy'
        sh 'kubectl apply -f manifest.yaml'
   }

}
