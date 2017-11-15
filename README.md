# pfda2dockstore

Export precisionFDA apps to Dockstore

Be sure to set these variables in your environment:

* PFDA_TOKEN (your PrecisionFDA token)
* GITHUB_TOKEN
* DS_TOKEN (your Dockstore token)

## pfda2dockstore

For example, to export [vcf-comparison](https://precision.fda.gov/apps/app-BqB9XZ8006ZZ2g5KzGXP3fpq) and save it in Github at [pfda2dockstore](https://github.com/pfda2dockstore) and DockerHub organization [pfda2dockstore](https://hub.docker.com/u/pfda2dockstore):

    conda create -n pfda python=3.5 anaconda
    source activate pfda
    pip install PyGithub agithub
    # alternatively, you can call run.sh or the two commands below
    docker login
    python pfda2dockstore --app-name vcf-comparison --pfda-token $PFDA_TOKEN --github-token $GITHUB_TOKEN --github-org pfda2dockstore --dockerhub-org pfda2dockstore --dockstore-token $DS_TOKEN

## Results

At this point take a look at your org in Github, DockerHub, and Dockstore.  You should see the vcf-comparison repo (or whichever tool you chose to export).



----


Inputs: Github Token, Quay.io token, reponame, list of files
