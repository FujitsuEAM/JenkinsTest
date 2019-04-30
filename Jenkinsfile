pipeline { 
    agent any 
	
	 parameters {
        boolean(defaultValue: "1", description: 'Install Pre Reqs?', name: 'PreRequistes')
		boolean(defaultValue: "1", description: 'Extract Files?', name: 'ExtractInstallationFiles')
        choice(choices: ['DEV', 'TEST', 'PROD'], description: 'Which Server to Deploy to?', name: 'ServerName')
    }
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('PreRequistes') { 
             when { 
                 expression 
                    { return params.PreRequistes } 
            }
            steps { 
                echo 'Pre req stage'
                echo params.ServerName
            }
            
        }
        stage('ExtractInstallationFiles'){
            when { 
                 expression 
                    { return params.ExtractInstallationFiles } 
            }
            steps {
                echo 'ExtractInstallationFiles stage'
				
            }
        }
        
    }
}