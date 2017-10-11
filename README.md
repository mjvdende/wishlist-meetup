PART 3
======

## GENERAL
In this part we will create the Jenkins build pipeline with all the automated build steps. We have added an incomplete 
pipeline file for you. You will have to complete this file. Afterwards we will commit all code to gitlab running on the 
kubernetes cluster and we will setup the Jenkins job for the continuous deployment. Lastly, we will run the pipeline 
and see the magic happen.   

### 1) Complete pipeline
Open the [Jenkinsfile](./frontend/Jenkinsfile) and add all the missing logic (marked with `complete step`) to complete 
the pipeline. 

Hint: remember all the npm scripts created in part 2 of this meetup.

### 2) Gitlab
Open gitlab in a browser and create a new public repository called `wishlist`.
* Gitlab user: root
* Gitlab password: whatever you choose

Note: you could also easily use a private repo with password or ssh key but that's not in scope for this meetup.

### 3) Commit code
Move into the frontend folder to commit all code to gitlab. To do so, follow the instructions given by gitlab. You can
see these instructions by opening the git project in gitlab.

Note: the given url by gitlab may deviate (for some reason Gitlab uses it's own generated repo urls). When you add 
remote make sure to use `http://$(minikube ip)/gitlab/root/wishlist.git`.  

### 4) Create Jenkins job
Now open Jenkins and create a new multi branch job called `wishlist`. Add the git source and save.

### 5) Run the job
Now trigger the pipeline and watch the magic happen.

Note: to see the full effect you could first delete the frontend from the Kubernetes cluster.

### Extra) Multi branch
Create a new feature branch and see how the Jenkins pipeline deals with it. 

## END PART 3
Congratulations, you have reached the end of this meetup! You can checkout the branch named `complete` to see all parts
completed.