pipeline{
    agent {
        label{
            label 'built-in'
            customeWorkspace '/mnt/2026Q1'
        }
    }
    stages{
        stage('clean'){
            steps{
                sh 'chmod -R 777 /var'
                sh 'rm -rf /var/www/html'
                echo 'removing older index.html'
            }
        }
        stage('build'){
            steps{
                sh 'cp -r index.html /var/www/html'
                echo 'pasted new index.html in /var/www/html'
            }
        }
        stage('deploy'){
            steps{
                sh 'service httpd start'
                echo 'deployed'
            }
        }
    }
}
