# Leiningen ClickStack

For all your Leiningen needs!

## Creating an app

For this to work, you will need to have the CloudBees SDK installed. 
Here, we simply create a new application on CloudBees.

    bees app:create APP_NAME

## Deploying your Leiningen/Clojure application to the cloud!

You're almost done! Just specify the commands you'd like for Leiningen to run in your project directory package and deploy with:

    zip ../MYAPP.zip .
    bees app:deploy -Rargs="do clean, trampoline ring server-headless" -t lein -a APP_NAME ../MYAPP.zip

You can run whatever Leiningen commands you like. 

And your app is now running on the cloud!