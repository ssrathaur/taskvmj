node { 
stage ('input') { 

   def userInput = input message: 'enter git details',
     parameters: [
     string(defaultValue: 'dev', description: 'branch name', name: 'branch'),
     string(defaultValue: '', description: 'repo url', name: 'url')
     ]

    git branch: userInput['branch'], credentialsId: 'creds', url: userInput['url']
   }
}
