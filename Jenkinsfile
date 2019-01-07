node {  
   stage('Fetch') {
   echo 'Fetching code from github'
       git 'https://github.com/DeclanCarter/NewJenkins.git'
    }
        stage('Build'){
            steps{
			echo 'Building task'	
                bat '
        javac -cp "C:\\Users\\unumuser\\Desktop\\Jenkins\\lib\\junit-4.12.jar";"C:\\Users\\unumuser\\Desktop\\Jenkins\\lib\\hamcrest-core-1.3.jar";. "Student.java" "StudentTest.java"'
		}
    }
		stage('Test'){
		steps{
		echo 'Testing Task'
		  bat 
        'java -cp "C:\\Users\\unumuser\\Desktop\\Jenkins\\lib\\junit-4.12.jar";"C:\\Users\\unumuser\\Desktop\\Jenkins\\lib\\hamcrest-all-1.3.jar";. org.junit.runner.JUnitCore studentTest'
        
	  }
}

  post {
    success {
        echo 'Successful'
    } 
  failure {
  echo 'Errors had occurred'
}
}
}
