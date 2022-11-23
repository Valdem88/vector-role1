pipeline {
    agent {
        label 'linux'
    }
    stages {
        stage('Git') {
            steps{
                git branch: 'main', url: 'https://github.com/Valdem88/dev-17_ansible-04-role-yakovlev_vs.git'
            }
        }
        stage('Molecule install') {
            steps{
                sh 'pip install molecule==3.4.0'
                sh 'pip install "ansible-lint<6.0.0"'
                sh 'pip install molecule_docker'
            }
        }
        stage('cd roles') {
            steps{
                sh 'cd roles/vector-role/'
                
            }
        }
        stage('Molecule test'){
            steps{
                sh 'ls -l'
                cleanWs()
            }
        }
        
    }
}
