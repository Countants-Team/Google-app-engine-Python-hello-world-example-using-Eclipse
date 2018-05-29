# Google-app-engine-Python-hello-world-example-using-Eclipse
Step by step process for setup google app engine in eclpise, Run it locally and deploy it to Google App Engine account.

#### Tools required
Eclipse with pydev

[Download eclipse](https://www.eclipse.org/downloads/) and Install [pydev](http://www.pydev.org/)

In Eclipse , menu, “Help –> Install New Software..” and click on Add

![alt text](https://drive.google.com/uc?id=1FphKGMHJPC1bM0e2Sc6xmJhPBOvW_BMx)

Put URL http://pydev.org/updates and click Ok. Select “PyDev” option and click on Next restart Eclipse once completed.

![alt text](https://drive.google.com/uc?id=1zZgUS6K8pm1coP-FOMNu4sTmpIs98IP7)


#### Library required
1. Python 2.7
2. Google App Engine SDK for Python

Now Install [python 2.7](https://www.python.org/downloads/) and [Google App Engine SDK for Python](https://cloud.google.com/appengine/downloads#Google_App_Engine_SDK_for_Python)

Below steps to show you how to create a GAE project via Pydev plugin

1. Eclipse menu, File -> New -> project type pydev then choose “PyDev Google App Engine Project“. 

![alt text](https://drive.google.com/uc?id=1xSlvu2WfCzGUb55rcD_sYpFGVecCJpEq)

2. Type project name, if the interpreter is not configure yet you can do it now. And select this option – “Add Project directory to the PYTHONPATH“. click Next

![alt text](https://drive.google.com/uc?id=1_-FAyoI5NJpiLp5hQ_HDfZ331xJfYo_0)

3. Click “Browse” button and point it to the Google App Engine installed directory

![alt text](https://drive.google.com/uc?id=1H04PqeoRdRpopnCzP-_lDEeGKdFOjL0P)

4. Name your application id in GAE, type anything, you can change it later. And choose “Hello Webapp World” template to generate the sample files. click Finish

![alt text](https://drive.google.com/uc?id=1htGIkk6dPdzkZCX_Kf66ZRsr8UopXtYC)

5. Done, 2 files are generated, app.yaml(configuration file) and helloworld.py(python file)

![alt text](https://drive.google.com/uc?id=1xmzt3Iu0VPHaByufuNCwdB6hBegJ3Yp6)

6. To run it locally, right click on the helloworld.py, choose “Run As” –> “Run Configuration”, create a new “PyDev Google App Run“.
In Main tab -> Main module, manually type the directory path of “dev_appserver.py“. “Browse” button is not able to help you, type manually

![alt text](https://drive.google.com/uc?id=1FVJ2ZW0h0rZ2KDZ-Lp2jM_x9M5Vk2W40)

7. In Arguments tab -> Program arguments, put “${project_loc}/src“.

8. Click on Apply.

9. Run it. By default, it will deploy to http://localhost:8080.

![alt text](https://drive.google.com/uc?id=1nh5syHJbxhY5ogMVfftjFELLrOxNA_7T)

10. Done. Copy url and paste into the browser.

![alt text](https://drive.google.com/uc?id=13sFS-IWknUORBjY8dqOiIW668QQsO9EM)


#### Deploy to Google App Engine

1. Register an account on [Google App Engine](https://appengine.google.com/) and create application ID.
2. Open your “app.yaml” file. Replace your application field with your application ID.

```
application: sample-app
version: 1
runtime: python27
# threadsafe is required but can be either true or 
# false. For some package, it should be true e.g. Flask
threadsafe: true
api_version: 1

handlers:
- url: /.*
  script: helloworld.app
  ```

3. Create another new “PyDev Google App Run”, In Main tab -> Main module, manually type the directory path of “appcfg.py“.

![alt text](https://drive.google.com/uc?id=1V2gOiC0fU5gJ7UPpm5bn5XerKYBmpBfn)

4. In Arguments tab -> Program arguments, put “update ${project_loc}/src“.

![alt text](https://drive.google.com/uc?id=1VtwN-8K3fQtCL6LmgPmfS_ux4WzG2LXR)

5. During deployment process you need to have your GAE email and password for authentication. it'll redirect automatic for authentication.

6. Run your app with URL - https://<your app id>.appspot.com




