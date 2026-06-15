pipeline{
   agent any
   
   tools{
   maven 'Maven'
   }
   
   stages{
   stage('Checkout'){
   steps{
   git branch:'main',url:"https://github.com/amruthar77/MavenSeleniumLast.git"
   }
   }
   
   stage('Build'){
   steps{
   sh 'mvn clean package'
   }
   
   }
   
   stage('Test'){
   steps{
   sh 'mvn test'
   }
   }
   
   stage('Run Selenium')
   {
   steps{
   sh 'mvn exec:java -Dexec.mainClass="com.example.App" '
   }
   }
   }
   
   post{
   success{
   echo "open saudemo.com: https://www.saucedemo.com/"
   }
   failure{
   echo "failure"
   }
   }
   }
