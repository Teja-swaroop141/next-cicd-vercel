pipeline{
    agent any

    environment {
        VERCEL_TOKEN=credentials('vercel_token')
    }

    stages{
        stage('install'){
            steps{
                bat 'npm install'
            }
        }
        stage('Test'){
            steps{
                ech 'no test found'
            }
        }
        stage('build'){
            steps{
                bat 'npm run build'
            }
        }
        stage('deploy'){
            steps{
                bat 'npx vercel --prod --yes --token=%VERCEL_TOKEN%'
            }
        }
    }
}