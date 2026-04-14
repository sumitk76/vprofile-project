pipeline {
    agent any
    tools {
        maven "MAVEN3.9.9"
        jdk "JDK17"
    }
    
    environment {
        SNAP_REPO = 'vprofile-snapshot'
		NEXUS_USER = 'admin'
		NEXUS_PASS = 'Rchik@6824'
		RELEASE_REPO = 'vpro-release'
		CENTRAL_REPO = 'vpro-proxy'
		NEXUSIP = '192.168.56.10'
		NEXUSPORT = '8081'
		NEXUS_GRP_REPO = 'vpro-gr'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}
