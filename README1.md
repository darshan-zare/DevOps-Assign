

Build Trigger  --> using  Webhook
	Whenever we do modifications in our project or whenever we do changes in the code and that changes when we push to our repository (Github) build has to Trigger automatically.

Download ngrrok  (https://ngrok.com/download) (according to ur OS)
Open cmd prompt from wherever your ngrok is downloaded
run command  --> ngrok http jenkinsportnumber <--
		ex.    ngrok http 8001
Then copy the link 
		ex.    https://ab8259eca344.ngrok.io
Then go to github..
go to your project setting
click on Webhook ->  Add Webhook -> paste the link  under payload  url which is copied from ngrok command prompt then append /github-webhook/ to that link
	ex. https://ad28e1399d19.ngrok.io/github-webhook/
Then click on Add webhook.

Go to Jenkins
Go to your project configuration -> Source Code Management -> git -> add your project github project url
Add your github credentials
Under Build Triggers tickmark   -GitHub hook trigger for GITScm polling-
Apply and Save

Then do modifications in your project or in your code  from gitbash command prompt or manually in files 
Then observe the jenkins you will see the build triggered. 



