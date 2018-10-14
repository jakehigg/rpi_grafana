pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh "docker build -t local/grafana:latest ."
            }
        }
	stage('Tag') {
	    steps {
		sh "docker tag local/grafana:latest 10.10.104.32:5000/grafana:latest"
	   }
	}
	stage('Push') {
	    steps {
		sh "docker push 10.10.104.32:5000/grafana:latest"
	    }
	}
     }
}
