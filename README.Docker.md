### Clone the Moodle repository
First clone the git repository. Since moodle is quite big in size I did not include it with this repository. You can clone the **Moodle v4.3** by the following command.
```bash
git clone https://github.com/moodle/moodle.git --branch MOODLE_403_STABLE
```

After you clone the moodle repository then you are 
### Building and running your application

When you're ready, start your application by running:
`docker compose up --build`.

Your application will be available at http://localhost:9000.

### Deploying your application to the cloud

First, build your image, e.g.: `docker build -t myapp .`.
If your cloud uses a different CPU architecture than your development
machine (e.g., you are on a Mac M1 and your cloud provider is amd64),
you'll want to build the image for that platform, e.g.:
`docker build --platform=linux/amd64 -t myapp .`.

Then, push it to your registry, e.g. `docker push myregistry.com/myapp`.

Consult Docker's [getting started](https://docs.docker.com/go/get-started-sharing/)
docs for more detail on building and pushing.