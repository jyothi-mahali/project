pipeline{
    agent any
    tools{
        maven "MAVEN3"
        jdk "java"
    }
    environment{
        SNAP_REPO = "project-snapshot"
        NEXUS_USER = "admin"
        NEXUS_PASS = "Nexus@123"
        RELEASE_REPO = "project-release"
        CENTRAL_REPO = "project-maven-central"
        NEXUSIP = "172.31.4.161"
        NEXUSPORT = "8081"
        NEXUS_GRP_REPO = "project-maven-group"
        NEXUS_LOGIN = "nexuslogin"
    }
    stages{
        stage('Build'){
            steps{
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}