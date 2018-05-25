<!--
#                                 __                 __
#    __  ______  ____ ___  ____ _/ /____  ____  ____/ /
#   / / / / __ \/ __ `__ \/ __ `/ __/ _ \/ __ \/ __  /
#  / /_/ / /_/ / / / / / / /_/ / /_/  __/ /_/ / /_/ /
#  \__, /\____/_/ /_/ /_/\__,_/\__/\___/\____/\__,_/
# /____                     matthewdavis.io, holla!
#
#-->

[![Clickity click](https://img.shields.io/badge/k8s%20by%20example%20yo-limit%20time-ff69b4.svg?style=flat-square)](https://k8.matthewdavis.io)
[![Twitter Follow](https://img.shields.io/twitter/follow/yomateod.svg?label=Follow&style=flat-square)](https://twitter.com/yomateod) [![Skype Contact](https://img.shields.io/badge/skype%20id-appsoa-blue.svg?style=flat-square)](skype:appsoa?chat)

# easy nginx

> k8 by example -- straight to the point, simple execution.

## Usage

```bash
$ kubectl apply -f manifests/

deployment "nginx" created
service "nginx" created

$ kubectl get pod,svc -lapp=nginx

NAME                                  READY     STATUS    RESTARTS   AGE
po/nginx-deployment-5ff7dc4cf-xqb8k   1/1       Running   0          13m

NAME        TYPE       CLUSTER-IP      EXTERNAL-IP   PORT(S)        AGE
svc/nginx   NodePort   10.11.254.110   <none>        80:31896/TCP   28m

$ nmap -Pn -p80 10.11.254.110

Starting Nmap 7.01 ( https://nmap.org ) at 2018-03-19 22:06 DST

Nmap scan report for 10.11.254.110
Host is up (0.053s latency).
PORT   STATE SERVICE
80/tcp open  http

Nmap done: 1 IP address (1 host up) scanned in 0.13 seconds
```