---
title: "Update"
date: 2023-04-29T18:08:02-03:00
draft: false
---

# Personal Update

What am I up to ? Well, I'm still working but these days I'm not exactly
doing the same kind of work I used to do back in the day.

It took me many years to actually manage to distance myself from the most
*manual* work. It's still manual in the sense that my main work tool is a
keyboard and I type at it the whole day, but I digress.

I still work with infrastructure but it took me some time to understand that
infrastructure now is not really *metal* (you do not really rack servers
yourself in a [datacenter](https://aws.amazon.com/what-is/data-center/)).

I used to work on a company which had it's own datacenter so when people
said that you worked with infrastructure there it most likely meant that
you got your hands dirty and went to that cold place where a really large
amount of servers live in order to mess with [servers](https://en.wikipedia.org/wiki/Server_(computing)),
 [cables](https://en.wikipedia.org/wiki/Networking_cables) and stuff.

Today I work on an *infrastructure* team but there's no real physical
infrastructure to be managed at all. We are using 100% cloud infrastructure
and the team I'm working on is one the teams which *creates* infrastructure
on the cloud by writing a bunch of [pseudo-code](https://developer.hashicorp.com/terraform/language).

We then use [a tool](https://www.terraform.io/) which reads this pseudo-code
and talks to the cloud provider [APIs](https://aws.amazon.com/what-is/api/) to
command it to actually spin up resources. These resources are things like
[clusters](https://www.redhat.com/en/topics/containers/what-is-a-kubernetes-cluster),
which are just a bunch of servers. [Virtual servers](https://www.redhat.com/en/topics/virtualization/what-is-a-virtual-machine)
as we are in a cloud context here.

We also happen to support some development teams by *debugging* what some
people also consider these days as *infrastructure code*, but which is not
exactly the same kind of infrastructure code our team writes.

This infrastrucuture code the development teams are writing are a bunch of
[YAML](https://en.wikipedia.org/wiki/YAML) which is used to [declaratively](https://kubernetes.io/docs/tasks/manage-kubernetes-objects/declarative-config/) create [*deployments*](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)
for the real application code they are also writing in a [more complete programming language](https://en.wikipedia.org/wiki/Java_(programming_language)).

Our team deploys and maintains the infrastructure (*the cluster*) under which
the development team's deployments run.

We also happen to deploy and maintain [a solution](https://argo-cd.readthedocs.io/en/stable/)
for doing [GitOps](https://www.redhat.com/en/topics/devops/what-is-gitops), which
is a fancy term to say that when someone commits this bunch of YAML to a [source
code repository](https://github.com/), this YAML code automatically gets synced to a cluster and
then the application deployments are magically created inside this cluster.

Aditionally, when the development teams have trouble with their deployments
we help them by troubleshooting these deployments in order to find out where's
the issue. They mostly seem to think the issue is in our layer of the
 infrastructure (*the cluster*).

Most of the time it turns out that the issue is not really in the cluster
but in the YAML files they are writing to do their deployments.

This is currently my day-to-day job. A mixture of multiple technologies which
no sane non-technicall people would like to talk about.
