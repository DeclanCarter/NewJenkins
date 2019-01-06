pipeline{
    agent any

    stages{
	
	
        stage('Build'){
            steps{
			echo 'Building task'
				
                bat '''
        javac -cp "C:\\Users\\unumuser\\Desktop\\Jenkins\\lib\\junit-4.12.jar";"C:\\Users\\unumuser\\Desktop\\Jenkins\\lib\\hamcrest-core-1.3.jar";. "source\\main\\java\\Student.java" "source\\test\\java\\StudentTest.java"
        '''
		}
    }
		stage('Test'){
		steps{
		echo 'Testing Task'
		  bat '''
        java -cp "C:\\Users\\unumuser\\Desktop\\Jenkins\\lib\\junit-4.12.jar";"C:\\Users\\unumuser\\Desktop\\Jenkins\\lib\\hamcrest-core-1.3.jar";. org.junit.runner.JUnitCore source\test\java\studentTest
        '''

	  }
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
