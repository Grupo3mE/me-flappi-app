pipeline {
    agent any
	stages {
	    stage('Preparando el ambiente') {
		    steps {
	    	sh 'ls -l'
            sh 'rm -r ./k8s-deployment'
            }
}
        stage('Obteniendo codigo fuente'){
            steps{
            sh 'git clone https://github.com/alearaoz/k8s-deployment.git'
        }
}
        stage('Desplegando la aplicacion'){
            steps{
            sh 'cd me-flappi-app'
            dir('cd me-flappi-app'){
            sh 'kubectl apply -f deployment.yml'}
            }
        }
    }
}