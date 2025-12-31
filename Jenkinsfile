pipeline { 
agent any 
tools { 
go 'gotest1' 
} 
environment { 
GO111MODULE='on' 
} 
stages { 
stage('Test') { 
steps { 
git 'https://github.com/maazsid243-ai/ci-cd-demo.git' 
sh 'go test ./...' 
} 
} 
stage('Build') { 
steps { 
git 'https://github.com/maazsid243-ai/ci-cd-demo.git' 
sh 'go build .' 
} 
} 
stage('Run') { 
steps { 
sh 'cd /var/lib/jenkins/workspace/full-cicd-go && go-webapp-sample &' 
} 
} 
} 
} 
