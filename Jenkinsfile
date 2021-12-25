node{
    stage('scm checkout'){
    git credentialsId: 'github-cred', url: 'https://github.com/nagarajshobha/ansibelejenkins.git'
    }
    stage('ansible playbook'){
        ansiblePlaybook become: true, credentialsId: 'sshdev', disableHostKeyChecking: true, installation: 'ansible', inventory: 'httpd.inv', playbook: 'httpd-playbook.yaml'
    }
}
