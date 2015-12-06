---
layout: post
title: 'TaskAdapter 2.11.1: support for self-signed SSL certificates used on Redmine servers'
date: '2015-10-07 00:35:00 -0700'
categories:
- release
- redmine
---


TaskAdapter 2.11.1 release brings basic support for invalid or self-signed
(or simply not recognized for whatever reason) SSL certificates used by Redmine servers.

This version will ignore any SSL certificate checks. This has obvious security implications,
but at least it allows people to start using TaskAdapter with their custom SSL certificates
(which can be a majority of all SSL certificates).

Plus minor UI bugfixes.
