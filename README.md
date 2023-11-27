# New-CI-CD-Pipeline-
I am creating new ci-cd pipeline from starting to end 
pipeline
{
agent any
stages
{
stage ('checkout')
{
steps 
{
git credentialsId: ' ',
url: 'github repository URL',
branch: 'main'
}
}

stage ('Build Docker')
{
steps
{
script
{
sh ''
echo 'Build Docker Image'
docker build -t abhishekf5/cicd-ec2:${Build_Number}.
...
}
}
}
stage('Push the artifacts')
{
steps
{
script
{
sh '''
echo 'Push to Repo'
docker push abhishekf5/cicd-ec2e:${BUILD_NUMBER}
'''
}
}
}


