pipeline{
    agent any

    stages{
        stage('Build'){
            steps{
			echo 'Building task'
                bat 'C:\Program Files\Java\jdk1.8.0_171\bin\Javac.exe -cp lib/junit-4.13-beta-1.jar;lib/hamcrest-core-2.1.jar;source/Student.java;. source/studentTest.java
        }
    }
		stage('Test'){
		steps{
		echo 'Testing Task'
		  bat 'C:\Program Files\Java\jdk1.8.0_171\bin\Java.exe -cp lib/junit-4.13-beta-1.jar;lib/hamcrest-core-2.1.jar;. org.junit.runner.JUnitCore studentTest'
      

	  }
}
  post {
    success {
        echo 'Successful'
    }
  }
}