pipeline {  
    agent any  
  
    stages {  
        stage('Checkout') {  
            steps {  
                git('https://github.com/bkmyth/SoftwareHw.git', branch: 'master', credentialsId: 'your-github-credentials-id')  
            }  
        }  
          
        stage('Build') {  
            steps {  
                // 假设你的项目有 setup.py 或 requirements.txt 来定义依赖  
                // sh 'pip install -r requirements.txt'
                sh 'source activate /home/ubuntu/anaconda3/envs/SE'  
                // 如果需要编译或其他构建步骤，可以在这里添加  
            }  
        }  
          
        stage('Test') {  
            steps {  
                // 运行你的测试套件，例如 pytest  
                sh 'python main.py'
                // sh 'pytest'  
            }  
        }  
          
        stage('Deploy') {  
            steps {  
                // 假设你有一个部署脚本 deploy.sh 或类似的机制  
                // 这里只是一个示例，你需要根据你的实际部署方式进行调整  
                // sh 'bash deploy.sh'  
                // deploy.sh 可能包含停止当前运行的服务、复制新代码、启动新服务等步骤  
            }  
        }  
    }  
}