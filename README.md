# SBT ClickStack

For all your Scala needs!

## Creating an app

For this to work, you will need to have the CloudBees SDK installed. 
Here, we simply create a new application on CloudBees.

    bees app:create APP_NAME

## Deploying your Scala application to the cloud!

You're almost done! Just specify the arguments you'd like for SBT, for example, with clean compile run, in your project directory package and deploy with:
(Note that the command will not yet be working, it's just an indication of how it will be done in the near future).

    zip ../MYAPP.zip .
    bees app:deploy -Rargs="clean compile run" -t sbt -a APP_NAME ../MYAPP.zip

Or, for example for a test play 2 server, change the last command to:

    bees app:deploy -Rargs="\"start \$app_port\"" -t sbt -a APP_NAME ../MYAPP.zip

And your app is now running on the cloud!