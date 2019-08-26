node {
   stage('Source checkout') {
      git 'https://github.com/AdityaSP/devopsdemo'
   }
   stage('mvn compile'){
       sh label: '', script: 'mvn install'
   }
   stage('deploy html file'){
       sh label: '', script: 'cp index.html /var/www/html/pipeline-adi-index.html'
   }
   stage('Publish test results'){
       junit 'target/surefire-reports/*.xml'
       
   }
   stage('Archive artifacts'){
       archiveArtifacts 'target/*.jar'
   }
}
