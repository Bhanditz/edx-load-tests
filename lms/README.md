#Instructions
These are the instructions to get the edX load tests up and running. Please follow the instructions step by step:

1. Clone the edx-load-tests git repo:

	```bash
	git clone https://github.com/appsembler/edx-load-tests
	cd edx-load-tests
	git checkout appsembler/azure
	```
	
2. Install pip and virtualenv if they're not installed already:

	```bash
	easy_install pip
	pip install virtualenv
	```
	
3. Create a virtual environment for python code and activate it:

	```bash
	/* in the edx-load-tests folder */
	virtualenv venv
	source venv/bin/activate
	```
	
4. Install the python package requirements:

	```bash
	pip install -r requirements.txt
	```
	
5. Run the locust server:

	```bash
	locust --host=http://your-edx-host.com -f lms/locustfile.py
	```
	
6. Open [http://localhost:8089/](http://localhost:8089/) in your browser and enter the required parameters and run the tests!

# Random observations
* need to enable swap on the server
* auto auth wasn't enabled in lms.envs.json
* I needed to add an extra package to requirements.txt of edx-load-test repo to make it work, so we now have an appsembler fork at https://github.com/appsembler/edx-load-tests , the branch name is appsembler/azure
* the links "view unit in studio" don't work (on course pages when logged in as staff@example.com)
* 
