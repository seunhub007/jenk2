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
                        echo "welcome to the production. Added Jenkins nowg"

                        sudo apt install nginx -y
                        sudo systemctl enable nginx
                        sudo systemctl start nginx
                        sudo systemctl restart nginx

                        sudo apt update

                        cd /var/www

                        sudo rm -rf html
                        sudo mkdir html

                        sudo git clone https://github.com/seunhub007/jenk2.git html

                   '''
            }
        }
    }
}
