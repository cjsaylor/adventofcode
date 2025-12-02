Similar to 2024, I'm using Deno via Jupyterlab to solve the Advent of Code for 2025.

Refer to the `2024` directory for the relavent Dockerfile to build in order to run these notebooks.

---

One note I discovered since coming back to this project. The local path `./work/<year>/<day>/inputfile` only works when
running the notebooks through VSCode's Jupyter extension.
When executing the notebooks within the Jupyterlab interface through the browser, the local path is relative to the
upper level folder, so the equivalent input path would be `./inputfile`.

To keep it consistent and executable from both places, the full path `/home/jovyan/work/<year>/<day>/inputfile` can be used.