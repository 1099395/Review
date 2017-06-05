
node {
  def mvnHome = tool 'maven3'
  def javaHome = "C:/Program Files/Java/jdk1.8.0_121/bin"
  stage ("Intial Preparation") {
    bat "echo Preparations are done -- ${mvnHome} --${javaHome} "
  }
  stage ("Build Code") {
   
    bat "cd C:/Users/1099395/Downloads/Review  && ${mvnHome}/bin/mvn clean package"
    bat "echo code is builded"
  }
}
