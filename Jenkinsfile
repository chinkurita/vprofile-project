pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK17"
    }
    environment {
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'password@12345'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vprofile-maven-central'
        NEXUS_GRP_REPO = 'vprofile-maven-group'
        NEXUSIP = '172.31.93.219'
        NEXUSPORT = '8081'
        NEXUS_LOGIN = 'nexuslogin'
    }
    stages {
        stage('Build') {
          steps {
            sh 'mvn -s settings.xml -DskipTests install'
                 }
        }

    }
}