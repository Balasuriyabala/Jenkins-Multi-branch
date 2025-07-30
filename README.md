# Jenkins-Multi-branch Pipeline



<img width="684" height="338" alt="image" src="https://github.com/user-attachments/assets/44c86cb6-6986-4a76-939c-1ac46ce5f52d" />


Pipeline Script:
pipeline {
    agent any

    parameters {
        string(name: 'BRANCH_NAME', defaultValue: 'main', description: 'Enter the branch name to build (e.g., dev or main)')
    }

    stages {
        stage('Git') {
            steps {
                echo "Cloning branch: ${params.BRANCH_NAME}"
                git branch: "${params.BRANCH_NAME}", url: 'https://github.com/Balasuriyabala/Jenkins-Multi-branch.git'
            }
        }
    }
}



It ask the user where to fetch code:




<img width="647" height="170" alt="image" src="https://github.com/user-attachments/assets/aa032068-3fee-4ea0-85aa-8c6ee990cd9d" />

    
