# GitHub Copilot Starter

This is a basic [Flask][Flask] web app to demonstrate the functionality of [GitHub Copilot][Copilot] as part of the sponsored [Making Better Hacks, Faster with GitHub Copilot][Presentation] presentation.

[Flask]: https://flask.palletsprojects.com/
[Copilot]: https://github.com/features/copilot
[Presentation]: https://docs.google.com/presentation/d/1iGk2JK5IZswqVW9ES3dFw074FEeSXUssHooaT3WthKM/edit

## Getting Started

### 1. Clone the Repository

To use this app, first, clone the package to your local machine.

    git clone https://github.com/mlh/copilot-starter

_If you're using Visual Studio Code, this can be done by using the command pallet (`Ctrl-⇧-P` / `⌘-⇧-P`) and selecting `Git: Clone`, then typing `mlh/copilot-starter`._

### 2. Install the required packages

Using pip, you'll need to install the packages this project uses. The following command reads the requirements from requirements.txt and installs them.

    pip install -r requirements.txt

_This assumes you have python and pip already installed, if you do not, you'll need to [install them](https://wiki.python.org/moin/BeginnersGuide/Download). On a Mac, you may need to type `pip3` rather than `pip`._

_If you're using Visual Studio Code, you can open a terminal by using the command pallet (`Ctrl-⇧-P` / `⌘-⇧-P`) and selecting `Python: Create Terminal`._ 

### 3. Run the Flask app

To run the Flask app, you can use the following command, this uses Flask to execute code in `app.py`.

    python -m flask run --debug

_This command will fail, see the [next steps, below](#2-fix-issues), for how to fix it._

## Trying out GitHub Copilot

GitHub Copilot has a number of great features you can try. GitHub has a great [Getting Started Guide](https://docs.github.com/en/copilot/using-github-copilot/getting-started-with-github-copilot) which covers some of the features this project covers.

In Visual Studio Code, you can access GitHub Copilot by using the Copilot key command `Ctrl-I` / `⌘-I`, this guide assumes you're using Visual Studio Code and makes suggestions as though you are.

### 1. Explain the code

Copilot can explain what code does, you can select a section of code or have it explain the whole file.

1. Highlight the code you want Copilot to explain.\
_With `app.py` open, try selecting all of it._
2. Open Copilot (`Ctrl-I` / `⌘-I`)
3. Type `/explain`. \
_You can have Copilot explain the file generally, or as specific questions like `/explain Why is is int() used?`_

This is great when you come across a project you've never seen before or if a teammate introduced a method with some functions you don't recognize.

### 2. Fix Issues

The Flask app as written has a bug in it which you'll see [if you run the app](#3-run-the-flask-app). You can have Copilot propose fixes.

1. Open Copilot (`Ctrl-I` / `⌘-I`)
2. Type `/fix`. \
_Copilot works even better if you give it an error message or highlight the part of the code that's broken, like `/fix TypeError: The view function did not return a valid response.`_

If you accept the change, you should (likely) now be able to run the application. With your [app running](#3-run-the-flask-app) and navigate to <https://localhost:5000/> you should see a string of numbers (the seconds since the Unix epoch).

### 3. Write Code

You can use Copilot to write code.

1. Open Copilot (`Ctrl-I` / `⌘-I`)
2. Give Copilot a prompt, like `add a route that shows hours since the epoch`.

Copilot will make a suggestion for code that will work. For a simple application like this one, it will most likely work perfectly. For more complicated applications you may need to evaluate the code yourself to make sure it does what you expect.

### 4. Suggest Code

Just like a human pair programmer, Copilot is actively along side you as you program. You can just type code and Copilot will suggest autocompletions.

1. Start writing a new function, typing something like `def days_since_epoch():`
2. Hit `Tab ↹` after Copilot makes a suggestion.

_Try making a companion route to go with this and have Copilot help you there._
