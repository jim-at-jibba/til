# Regenerating the aws-export file in an amplify project

When cloning an existing amplify project you will be missing the `aws-export.js` file as it is in 
you `.gitignore`.

To regeneate it, you need to `pull` the project. This will pull the config from the aws 
servers

`amplify env pull`
