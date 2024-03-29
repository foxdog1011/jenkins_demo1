pipeline {
    agent any

    stages {
        stage('拉取 GitHub 代码') {
            steps {
                echo '拉取代码...'
                // 这里可以使用 'checkout scm' 来拉取代码，如果 Jenkinsfile 是从 SCM 获取的
            }
        }
        stage('通过 Maven 构建项目') {
            steps {
                echo '构建中...'
                // 这里可以添加 Maven 构建命令，例如 'sh "mvn clean package"'
            }
        }
        stage('通过 SonarQube 进行代码检测') {
            steps {
                echo '代码检测中...'
                // 添加 SonarQube 分析命令
            }
        }
        stage('通过 Docker 构建 Image') {
            steps {
                echo 'Docker 构建中...'
                // 添加 Docker 构建命令，例如 'sh "docker build -t my-image ."'
            }
        }
        stage('将 Image 推送到 Harbor') {
            steps {
                echo '推送中...'
                // 添加 Docker 推送命令，例如 'sh "docker push my-image"'
            }
        }
    }
}
