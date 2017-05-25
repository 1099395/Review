
node {
  def mvnHome = tool 'maven3'
  def javaHome = tool 'Java8'
  stage ("Intial Preparation") {
    bat "echo Preparations are done"
  }
  stage ("Build Code") {
    //bat "cd C:/Users/1099395/Downloads/Review/Review && set "JAVA_HOME=$javaHome" && $mvnHome/bin/mvn install"
    echo "JDK: $JAVA_HOME"
   bat "echo code is builded"
  }
  stage ("Build Image") {
    withCredentials([[$class: "UsernamePasswordMultiBinding", usernameVariable: 'DOCKERHUB_USER', passwordVariable: 'DOCKERHUB_PASS', credentialsId: '1099395']]) {
      bat "docker login --username $DOCKERHUB_USER --password $DOCKERHUB_PASS"
    }
  }
}
