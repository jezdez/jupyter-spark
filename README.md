# jupyter-spark

Jupyter Notebook extension for Apache Spark integration.

Includes a progress indicator for the current Notebook cell if it invokes a
Spark job. Queries the Spark UI service on the backend to get the required
Spark job information.

![Alt text](/screenshots/ProgressBar.png?raw=true "Spark progress bar")

To view all currently running jobs, click the "show running Spark jobs"
button, or press ```Alt+S```.

![Alt text](/screenshots/SparkButton.png?raw=true "show running Spark jobs button")

![Alt text](/screenshots/Dialog.png?raw=true "Spark dialog")

A proxied version of the Spark UI can be accessed at
http://localhost:8888/spark.

## Installation

To install, simply run:

```
pip install jupyter-spark
jupyter serverextension enable --py jupyter_spark
jupyter nbextension install --py jupyter_spark
jupyter nbextension enable --py jupyter_spark
```

To double-check if the extension was correctly installed run:

```
jupyter nbextension list
jupyter serverextension list
```

For development and testing, clone the project and run from a shell in the
project's root directory:

```
pip install -e .
jupyter serverextension enable --py jupyter_spark
jupyter nbextension install --py jupyter_spark
jupyter nbextension enable --py jupyter_spark
```

To uninstall the extension run:

```
jupyter serverextension disable --py jupyter_spark
jupyter nbextension disable --py jupyter_spark
jupyter nbextension uninstall --py jupyter_spark
pip uninstall jupyter-spark
```
