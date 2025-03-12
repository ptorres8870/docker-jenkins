pipeline
Jenkinsfile
echo     agent any >> Jenkinsfile
echo     stages { >> Jenkinsfile
echo         stage('Checkout') { >> Jenkinsfile
echo             steps { >> Jenkinsfile
echo                 checkout scm >> Jenkinsfile
echo             } >> Jenkinsfile
echo         } >> Jenkinsfile
echo         stage('Build') { >> Jenkinsfile
echo             steps { >> Jenkinsfile
echo                 bat 'docker build -t mi-pagina-web .' >> Jenkinsfile
echo             } >> Jenkinsfile
echo         } >> Jenkinsfile
echo         stage('Deploy') { >> Jenkinsfile
echo             steps { >> Jenkinsfile
echo                 bat 'docker stop mi-contenedor ^|^| true' >> Jenkinsfile
echo                 bat 'docker rm mi-contenedor ^|^| true' >> Jenkinsfile
echo                 bat 'docker run -d -p 8080:80 --name mi-contenedor mi-pagina-web' >> Jenkinsfile
echo             } >> Jenkinsfile
echo         } >> Jenkinsfile
echo     } >> Jenkinsfile
echo
