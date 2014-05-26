---
layout: post
title: "Deploying to OpenShift Using Snap-CI"
date: 2014-01-28 09:10
comments: true
categories: ['continuous integration', 'tech', 'openshift', 'snap-ci']
---
As I mentioned in my last post, my project is using OpenShift, and so
far, we love it. Another tool we're using is [Snap-CI](snap-ci.com), which has incredibly seamless deployments to Heroku and AWS.

<img src="{{ root_url }}/images/snap_pipeline.png" />

Deploying to OpenShift was pretty simple as well. We created a build stage in Snap-CI and added some tasks to the new stage:

<img src="{{ root_url }}/images/snap_new_stage.png" />

By default OpenShift creates a copy of your existing Git repository. Each push to the new OpenShift repository triggers a deploy. In theory, this means that all we need to do is force a push to the OpenShift repository every time we want to deploy:

<div class="code">$ git push -f myopenshift.git</div>

However, access to OpenShift is done via SSH, which means that pushing looks
more like this:

<div class="code">$ git push -f ssh://myopenshift.git</div>

And which also means that Snap needs to know about our SSH key. In order
to have our SSH key present when pushing, we first created an
environment variable in Snap called OPENSHIFT_SSH, which we echoed to a
file in the repository:

<div class="code">$ echo "$OPENSHIFT_SSH" > ./ssh_pk_file
<br/>$ chmod 600 ssh_pk_file</div>

We also had to change the permissions of the private key file.

Finally, we had a script that allowed us to specify the SSH key to use for
pushing to OpenShift:

<div class="code">$ ./script/my_git.sh -i ssh_pk_file push -f ssh://myopenshift.git</div>

We based our script off the one found [here](http://alvinabad.wordpress.com/2013/03/23/how-to-specify-an-ssh-key-file-with-the-git-command/). All it does is take in a git command with a parameter (-i) that allows you to specify which SSH key you'd like to use.

Our final list of tasks to execute for our integration build step
looks like this:

<div class="code">$ echo "$OPENSHIFT_SSH" > ./ssh_pk_file 
<br/>$ chmod 600 ssh_pk_file
<br/>$ ./script/my_git.sh -i ssh_pk_file push -f ssh://myopenshift.git</div>

Right now we have every push to our project git repository deploying to
our integration environment via Snap. When we choose, we can then deploy to
production, using the same steps as above.

<img src="{{ root_url }}/images/snap_integracion.png" />
