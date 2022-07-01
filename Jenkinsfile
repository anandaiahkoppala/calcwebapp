node{
    stage('environment'){
        PATH = "/opt/maven/bin/mvn:$PATH"
    stage('Git Clone'){
        git 'https://github.com/anandaiahkoppala/calcwebapp.git'
    }
    stage('Maven Package'){
        def mvnHome = tool name: 'Maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deployment'){ 
        sh 'cp target/*.war /opt/tomcat/webapps'
    }    
}
