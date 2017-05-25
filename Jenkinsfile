
node {
  def mvnHome = tool 'maven3'
  def javaHome = tool 'Java8'
  stage ("Intial Preparation") {
    bat "echo Preparations are done"
  }
  stage ("Build Code") {
   sh "cd C:/Users/1099395/Downloads/Review/Review && export JAVA_HOME=/tools/jdk1.8.0_121/ && /tools/apache-maven-3.3.9/bin/mvn clean package"
    //bat "cd C:/Users/1099395/Downloads/Review/Review &&  && ${mvnHome}/bin/mvn install"
    //echo "JDK: $JAVA_HOME"
   bat "echo code is builded"
  }
  stage ("Build Image") {
    withCredentials([[$class: "UsernamePasswordMultiBinding", usernameVariable: 'DOCKERHUB_USER', passwordVariable: 'DOCKERHUB_PASS', credentialsId: '1099395']]) {
      bat "docker login --username $DOCKERHUB_USER --password $DOCKERHUB_PASS"
    }
  }
}
