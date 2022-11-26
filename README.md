#### How to use ?

Steps to launch the jupyter lab interface with the right dependencies:

- Go to the deployment directory : ``` cd Docker_Deployment ```

- Build image with the command :
```docker build . -t nom_de_mon_image```

- Come back to the first directory source : ``` cd .. ```

- Run image with the command :
```docker run -it -v $(pwd):/home/my_notebooks -p 8888:8888 nom_de_mon_image```

For Windows : %cd%
For Powershell terminal : ${pwd}

- Go to the link specified in the terminal : http://127.0.0.1:8888/ ...

- The volume of my_notebooks in the Jupyter Lab should be synchronized with the working directory,
for running scripts, storing files...

----

To execute the notebook, you must identify yourself to your Google'account : 

- Log in to your google account first

- Launch the first two cells and go to the indicated address

- Retrieve the token by following the instructions and clicking on accept

- Copy the token in the output of the cell


