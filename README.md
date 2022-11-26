#### How to use ?

- First, store your xslx files in the "DataFrames" folder

- Verify your user's parameters in the programm... ('LFI', 'Satellite'...)


For deployments with a docker image :

##### OPTION 1 / On a local jupyter lab interface

Steps to launch the jupyter lab interface with the right dependencies:

- Go to the deployment directory : ``` cd Docker_Deployment ```

- Build image with the command :
```docker build . -t my_image_name```

- Come back to the first directory source : ``` cd .. ```

- Run image with the command :
```docker run -it -v $(pwd):/home/my_notebooks -p 8888:8888 my_image_name```

(For Windows : %cd% / For Powershell terminal : ${pwd} )

- Go to the link specified in the terminal : http://127.0.0.1:8888/ ...

- The volume of my_notebooks in the Jupyter Lab should be synchronized with the working directory,
for running scripts, storing files...

----

To execute the notebook, you must identify yourself to your Google'account : 

- Log in to your google account first (and you must have a account on GCP and activate the API Google Earth Engine)

- Launch the first two cells and go to the indicated address

- Retrieve the token by following the instructions and clicking on accept

- Copy the token in the output of the cell


##### OPTION 2 / Use the script .py

You can also use the script 'SAT_images...'.py 

But you have to :

- Install and gcloud CLI for the authentification (https://cloud.google.com/sdk/docs/install#linux)

- install all the dependencies in your local host machine... or run the docker image in the folder 'Docker_Deployment_local'... Then, go to the bash, install the CLI gcloud, and launch the script from the environnement...
