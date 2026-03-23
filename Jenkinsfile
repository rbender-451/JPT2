pipeline {
 agent {label "linux"}
  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
    disableConcurrentBuilds()
  }
  stages {
    stage('Hello') {
      steps {
        echo "hello"
      }
    }
   stage('list folders') {
    steps {
     script {
      def folderList = sh(script: "ls -d */", returnStdout: true).trim()
      echo "Folders found: ${folderList}"
     }
    }
   }
  }
}
