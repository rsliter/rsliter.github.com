---
layout: post
title: "Deploying a Rails App with OpenShift"
date: 2014-01-27 09:48
comments: true
categories: ['tech', 'rails', 'openshift', 'passenger']
---

My current project is a Rails codebase that is deploying to OpenShift.
Overall we've been very pleased with OpenShift, however, it's a little
misleading how the first thing you see when you sign up is a prompt to
deploy your first application by simply providing a link to the
hosted code on GitHub.

<img src="{{ root_url }}/images/openshift_create.jpg" />

<!--more-->

Unfortunately, if you do that, you'll probably get a stack trace that looks
like this:
<img src="{{ root_url }}/images/openshift_passenger_error.jpg" />

With this error:
```
/opt/rh/ruby193/root/usr/share/gems/gems/passenger-3.0.17/helper-scripts/prespawn:105:in `initialize': Connection refused - connect(2) (Errno::ECONNREFUSED)</p>
```

That's because OpenShift requires some additional files to be included
in your application before it can be run. I needed to add a directory to
the application called .action_hooks and change the production settings
in the database configuration file. Check out their [example Rails project](https://github.com/openshift/rails-example) on GitHub to get the default action hooks and database configuration.
