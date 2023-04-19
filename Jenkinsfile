pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('初始化') {
            steps {
                echo "开始构建"
            }
        }
        stage('构建') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('打包') {
            steps {
                echo "开始打包"
            }
        }
        stage('测试') {
            steps {
                echo "开始测试"
            }
        }
    }
}