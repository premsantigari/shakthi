pipeline{
	agent any
	tools {
		maven 'MAVEN3.8.6'
	}
	environment{
		SNAPSHOT_REPO= 'prem-snapshot'
		NEXUS_USER= 'admin'
		NEXUS_PASS= '12345'
		CENTRAL_REPO= 'prem-maven-proxy'
		RELEASE_REPO= 'prem-pro'
		NEXUSIP= '172.31.14.178'
		NEXUSPORT= '8081'
		NEXUS_GRP_REPO= 'prem-maven-group'
		NEXUS_LOGIN= 'Nexusrepository'
	}
	stages{
	    stage('Build'){
	        steps{
	            sh 'mvn -s settings.xml -DskipTests install'
	        }
	    }
	}
}
