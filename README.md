# python-tools
<h3>Create a folder "dev-tools" and store the tools below.</h3>
<h4>Must</h4>
1. 	instantclient_19_11
	Database
2. 	Miniconda3
	Python enviroment

<h4>Opinional</h4>
1.	pw-browsers
	Playwright browsers for automation health check
2.	tika-app-2.1.0.jar
	Apache Tika

<h3>Set Python Enviroment</h3>
<h4>Edit "launch.bat"</h4>

set "PLAYWRIGHT_BROWSERS_PATH=%CD%\dev-tools\pw-browsers"	<- Playwright
set "__MINICONDA__=%CD%\dev-tools\Miniconda3"				<- Python Enviroment
set "__CX_ORACLE__=%CD%\dev-tools\instantclient_19_11"		<- Oracle Database
set "__TIKA_JAR__=%CD%\dev-tools\tika-app-2.1.0.jar"		<- Apache Tika

<h5>Python Setting</h5>
set "TNS_ADMIN="
set "PATH=%__MINICONDA__%;%__MINICONDA__%\Scripts;%__MINICONDA__%\Library\bin;%__CX_ORACLE__%;%PATH%"
set "PYTHONPYCACHEPREFIX=%CD%\python-cache"

<h5>Create folder to store data</h5>
mkdir "%CD%\python-cache"
mkdir "%CD%\src"
mkdir "%CD%\src\downloads"
mkdir "%CD%\src\screenshots"

cd "%CD%\src"
set "PYTHONPATH=%CD%"
cd "%BACKUP_CD%"

<h5>Install libriary to miniconda based on you need.</h5>
REM conda update conda --all
REM conda create --name testing python=3.9              
REM Use miniconda to create a virual environemt with python version 3.9
REM conda config --add channels microsoft 
REM conda config --add channels conda-forge
REM conda install -c conda-forge cx_oracle 
REM conda install -c microsoft playwright
REM conda install -c conda-forge pytest
REM conda install -c conda-forge requests
REM conda install -c conda-forge pywin32

REM playwright install
cmd "/K" activate.bat testing        <- Activate virual environment named testing                   
