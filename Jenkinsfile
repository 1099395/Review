
node {
  def mvnHome = tool 'maven3'
  def javaHome = tool 'Java8'
  stage ("Intial Preparation") {
    bat "echo Preparations are done"
  }
  stage ("Build Code") {
    bat "cd C:/Users/1099395/Downloads/Review/Review && set C:/Program Files/Java/jdk1.8.0_121 && ${mvnHome}/bin/mvn clean package"
   bat "echo code is builded"
  }
  stage ("Build Image") {
    withCredentials([[$class: "UsernamePasswordMultiBinding", usernameVariable: 'DOCKERHUB_USER', passwordVariable: 'DOCKERHUB_PASS', credentialsId: '1099395']]) {
      bat "docker login --username $DOCKERHUB_USER --password $DOCKERHUB_PASS"
    }
  }
}
