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
   stage('Load Local File') {
      steps {
       script {
        def utils = load '/home/pulsepointer/Documents/HelloWorld.groovy'

        utils.sayHello('Jenkins')
       }
      }
     }
  }
}
