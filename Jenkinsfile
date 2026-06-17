pipeline{
agent any
tools{
maven 'Maven'
}
stages{
stage('Checkout'){
steps{
git branch:'master',url:'https://github.com/Samiksha201104/MySeleniumP.git'
}}
stage('Build')
{
steps{
sh 'mvn clean install'}}
stage('Test')
{
steps{
sh 'mvn test'
}}
stage('Run App')
{
steps
{
sh 'mvn exec:java -Dexec.mainClass="com.example.App" '
}}}
post
{
success{
echo 'Buuild Success'
}
failure
{
echo 'failure'
}
}
}
