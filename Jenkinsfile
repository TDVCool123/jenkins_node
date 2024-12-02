pipeline {
    agent any
    tools{
        nodejs 'Node 18.x'
    }
    stages {
        stage('Checkout') {
            steps {
                echo 'Clonando el repositorio...'
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                echo 'Instalando dependencias...'
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                echo 'Construyendo la aplicación...'
                sh 'npm run build || echo "No hay pasos de construcción definidos"'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Desplegando la aplicación...'
                sh 'echo "Despliegue simulado completado"'
            }
        }
    }
    post {
        success {
            echo 'Pipeline completado con éxito.'
        }
        failure {
            echo 'El pipeline falló. Revisa los errores.'
        }
    }
}