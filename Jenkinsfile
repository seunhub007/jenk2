pipeline{
    agent any
    stages{
        stage('test'){
            steps{
                sh '''
                        echo "welcome to the test"
                   '''
            }
        }

        stage('production'){
            steps{
                sh '''
                        echo "welcome to the production. Added Jenkins"

                        sudo apt-get install nginx -y
                        sudo systemctl start nginx

                        sudo apt-get update -y

                        cd /var/www

                        sudo rm -rf html
                        sudo mkdir html

                        sudo git clone https://github.com/seunhub007/jenk2.git

                   '''
            }
        }
    }
}
