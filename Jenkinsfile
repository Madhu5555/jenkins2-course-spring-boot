pipeline {
  agent any
  stages {
    stage('Source') { 
      steps {
			// Some Step
      checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/g0t4/jenkins2-course-spring-boot.git']]])
      }
    }
    stage('Compile') { 
      tools {
        // Specify Tool Name from your global tool configuration
		jdk 'jdk8'
        maven 'Maven'
      }
      steps {
			// Some Step
	      powershell label: '', script: 'mvn clean package'
      }
    }
  }
}
