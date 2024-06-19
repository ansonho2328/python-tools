# python-tools
<h3>Create a folder "dev-tools" and store the tools below.</h3>
<h4>Must</h4>
1. 	instantclient_19_11<br/>
	Database<br/>
2. 	Miniconda3<br/>
	Python enviroment

<h4>Opinional</h4>
1.	pw-browsers<br/>
	Playwright browsers for automation health check<br/>
2.	tika-app-2.1.0.jar<br/>
	Apache Tika

<h3>Set Python Enviroment</h3>
<h4>Edit "launch.bat"</h4>

set "PLAYWRIGHT_BROWSERS_PATH=%CD%\dev-tools\pw-browsers"	<- Playwright<br/>
set "__MINICONDA__=%CD%\dev-tools\Miniconda3"				<- Python Enviroment<br/>
set "__CX_ORACLE__=%CD%\dev-tools\instantclient_19_11"		<- Oracle Database<br/>
set "__TIKA_JAR__=%CD%\dev-tools\tika-app-2.1.0.jar"		<- Apache Tika

<h5>Python Setting</h5>
set "TNS_ADMIN="<br/>
set "PATH=%__MINICONDA__%;%__MINICONDA__%\Scripts;%__MINICONDA__%\Library\bin;%__CX_ORACLE__%;%PATH%"<br/>
set "PYTHONPYCACHEPREFIX=%CD%\python-cache"

<h5>Create folder to store data</h5>
mkdir "%CD%\python-cache"<br/>
mkdir "%CD%\python-tools"<br/>
mkdir "%CD%\python-tools\downloads"<br/>
mkdir "%CD%\python-tools\screenshots"<br/>
<br/>
cd "%CD%\python-tools"<br/>
set "PYTHONPATH=%CD%"<br/>
cd "%BACKUP_CD%"

<h5>Install libriary to miniconda based on you need.</h5>
REM conda update conda --all<br/>
REM conda create --name testing python=3.9<br/>
REM Use miniconda to create a virual environemt with python version 3.9<br/>
REM conda config --add channels microsoft <br/>
REM conda config --add channels conda-forge<br/>
REM conda install -c conda-forge cx_oracle <br/>
REM conda install -c microsoft playwright<br/>
REM conda install -c conda-forge pytest<br/>
REM conda install -c conda-forge requests<br/>
REM conda install -c conda-forge pywin32<br/>
<br/>
REM playwright install<br/>
cmd "/K" activate.bat testing        <- Activate virual environment named testing                   
