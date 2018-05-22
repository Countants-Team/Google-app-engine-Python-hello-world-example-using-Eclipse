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

4. Name your application id in GAE, type anything, you can change it later. And choose “Hello World GAE” template to generate the sample files. click Finish

![alt text](https://drive.google.com/uc?id=19AJfSPQ4HWzJnEQ3SOkUJIq2duTpG7JP)

