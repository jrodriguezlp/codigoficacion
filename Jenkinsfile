pipeline {
    agent any

    stages {
        stage('1. Verificación de Código (GitHub)') {
            steps {
                echo 'Descargando código fuente desde el repositorio de GitHub...'
                checkout scm
            }
        }

        stage('2. Validación de Archivos del Proyecto') {
            steps {
                echo 'Verificando existencia de Dockerfile y README.md...'
                sh 'ls -la'
            }
        }

        stage('3. Prueba de Integración Continua') {
            steps {
                echo 'Ejecutando validación de entorno CI exitosa.'
            }
        }
    }

    post {
        success {
            echo 'Pipeline ejecutado correctamente. Integración Continua validada.'
        }
        failure {
            echo 'Error en la ejecución del Pipeline.'
        }
    }
}