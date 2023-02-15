pipeline{
  agent{
    docker { image 'openjdk:11' }
  }
  
  stages{
    stage('GIT CLONE'){
      steps{
        sh 'git clone https://github.com/notarnic/test_jenkins_java.git'
        sh 'cd test_jenkins_java'
        sh 'javac Prova.java'
        sh 'jar cfvm TestJar.jar manifest *.class'
        sh 'java -jar TestJar.jar'
      }
    }
  }
}
