pipeline { 
    agent any 
	
	 parameters {
        booleanParam(defaultValue: true, description: 'Install Pre Reqs?', name: 'PreRequistes')
		booleanParam(defaultValue: true, description: 'Extract Files?', name: 'ExtractInstallationFiles')
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