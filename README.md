# GenAI-bedrock
this is a simple Generative AI project in which I have used Amazon Bedrock's foundational model Llama3 70b to generate a 200-word blog on a blog_topic, by getting a lambda function to get triggered by a Post request using API gateway and the generated 200 words get stored in an S3 bucket this readmes gives a run down on how i went about it.

![Untitled Diagram](https://github.com/user-attachments/assets/09e2966b-f52b-460e-adf9-5ea65a31613e)

1. Create a virtual environment for python
	Why use a venv
	 -  Essentially there are modules that others have written and we do not want to rewrite those, which of course is time-consuming. 
          - Also you want to avoid conflict between package versions and it keeps your python environment clean    and organized
          - Isolation is important for safe testing and development, making possible for one work on tons of projects with different requirements affecting one another or your system's global Python installation.

	
	There are a couple of ways to get this done and inion, anaconda would give you optimal management for your virtual environment that you create and you can have different virtual environments created which need different versions of python and not only the one you have downloaded in your system
	3 ways are;
	     a. Python -m venv <name>
	      then activate from the activate file in the scripts directory. This method gives you     dependencies for the specific python version that you have installed.
	    b. Install venv   
	     virtual env -p python3 <name>
	     activate
	      virtual_env\Scripts\activate (you can actually use the relative path)
	     c. Install anaconda which is my favourite because it has a proper     management of environments that you create. When working with a project that has different python dependencies that require different versions of python, in order to avoid breaking things 
	Note: When you download Anaconda it will give you issues you would need to set the path correctly if not you would encounter errors or you reinstall and specify the path in environment variables. It will be in the users directory 
	C:\users\anaconda3  add in the path, the copied path and add Scripts C:\users\anaconda3\Scripts 
	
	
	
	
	n my humble opi
	




How to Fix the "Conda Command Not Recognized" Issue on Windows 10 | pythontwist.com


Create a venv 
Conda create -p <name > python==3.12
Conda activate <venv path>
Pip install -

Amazon Bedrock
Go to Amazon bedrock and cross check if the model you want to use is available in that region. For this project i went for Llama3-70b. Rem that there are important values that you must pass in the lamdba code from the llama model you have chosen. But first you  get model access at the bottom left of the screen

![image](https://github.com/user-attachments/assets/0d282ef1-9e53-4125-93a4-b019480b1311)
