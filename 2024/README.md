This year I'm solving these puzzles via Jupyter notebooks.

I've set up a custom jupyter notebook server at home with a Deno kernal enabled.

See the Dockerfile for specific package installation details.

Each day will be it's own notebook.

## Lab notebook setup

Build the image for the base of the lab:

```
docker build . -t cjsaylor/deno-notebook
```

Start a container using the above built image mounting the project on the `jovean` work directory:

```
docker run -d --name deno-notebook -p 8888:8888 -v "${PWD}":/home/jovyan/work cjsaylor/deno-notebook
```

Access the logs to get the access token:

```
docker logs -f deno-notebook
```

It should be available at `http://localhost:8888`