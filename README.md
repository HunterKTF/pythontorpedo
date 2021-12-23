# pythontorpedo
Repo de la madre de scrum

Torpydo
A simple game of Battleship, written in Python.

Getting started
This project requires Python 3.6 or newer. To prepare to work with it, pick one of these options:

Linux and macOS
Create and activate a virtual environment . This assumes python3 is already installed.

python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
export PYTHONPATH=.
If you stop working on this project, close your shell, and return later, make sure you run the source bin/venv/activate command again.

Windows
Download  and install Python 3.6 for Windows. Make sure python is on your PATH. Open a command prompt:

python -m venv venv
venv\Scripts\activate.bat
pip install -r requirements.txt
set PYTHONPATH=.
Docker
If you don't want to install anything Python-related on your system, you can run the game inside Docker instead.

Build the Docker Image
docker build -t torpydo .
Run a Docker Container from the Image
docker run -it --env PYTHONPATH=/torpydo -v ${PWD}:/torpydo torpydo bash
Launching the game
python -m torpydo

# alternatively:
python torpydo/battleship.py
Running the Tests
nosetests --exe
behave
to run with coverage:

nosetests --cover-package torpydo --exe --with-coverage  --cover-html
to run and store the test results for further examination (e.g. build pipeline)

nosetests --exe --with-xunit
behave --junit
Run behave tests with coverage:

https://stackoverflow.com/a/37447392/736079
