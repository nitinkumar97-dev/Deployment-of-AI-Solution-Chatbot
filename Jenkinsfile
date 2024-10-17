pipeline {
    agent any 
    stages {
        stage('Clone Repository') {
            steps {
                // Clone the repository
                git url: 'https://github.com/nitinkumar97-dev/Deployment-of-AI-Solution-Chatbot.git', credentialsId: 'github-token'
            }
        }
        stage('Install Dependencies') {
            steps {
                // Navigate to the project directory and install dependencies
                dir('Deployment-of-AI-Solution-Chatbot') {
                    sh 'pip install -r requirements.txt'
                }
            }
        }
        stage('Run Streamlit App') {
            steps {
                // Run the Streamlit app
                dir('Deployment-of-AI-Solution-Chatbot') {
                    sh 'streamlit run app.py &'
                }
            }
        }
    }
}
