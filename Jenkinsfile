pipeline{
  agent any
  tools{
    maven "Maven"
    jdk "JDK"
  }
  stages{
  stage('checkout'){
    steps{
      git "https://github.com/HackStyx/maven-lab-1.git"
    }
  }
    stage('build'){
      steps{
        sh 'mvn clean install'
      }
    }
    stage('test'){
      steps{
        sh 'mvn clean test'
      }
    }
    stage('run'){
      steps{
        sh 'mvn exec:java -Dexec.mainClass="com.example.app.App"'
      }
    }
  }
}
