
node('node1') {
    
    def mavenHome=tool name: "maven3.6.3"
    
    stage('CheckoutCode'){
     git branch: 'dev', credentialsId: 'GItHubCredentials', url: 'https://github.com/Alteon-demoapporg/Adv-app-project.git'
    }
    stage('build'){
        sh "${mavenHome}/bin/mvn clean package"
    }
    stage('ExecuteSonarQubeReport'){
        sh "${mavenHome}/bin/mvn sonar:sonar"
        
    }
}
