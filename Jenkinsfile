pipeline {
    agent any

    stages {
        stage('CreatingMLModelandUploadS3') {
            steps {
                git branch: 'main', url: 'https://github.com/NokkuPrudhvi/Create-ML-model-TRLabs.git'
                sh 'python3 ml_model.py'
                sh 'aws s3 cp ml_model.joblib s3://ml-models-bucket-345/ml_model.joblib'
            }
        }
    }
}
