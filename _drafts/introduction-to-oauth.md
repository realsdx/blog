---
layout: post
title: Introduction to OAuth2.0 protocol with VueJS and DRF
categories: [Authenticaion, Django]
---
## TL;DR;
Sadly, there is no copy-paste *code snippet* that you can use. This is not an ultimate guide for OAuth. This article will try to explain OAuth flow for a very specific(most common) senario.


Now, before jumping into the specific use case, lets try to understand What is it? and Why is everyone using it?
TODO: give an real world example

## What is OAuth ?

> OAuth is an open standard for access delegation, commonly used as a way for Internet users to grant websites or applications access to their information on other websites but without giving them the passwords.This mechanism is used by companies such as Google and Facebook to permit the users to share information about their accounts with third party applications or websites. 

Didn't get it? don't worry. Definations always sucks. <br />

Let's see an example, <br />

You (resource owner) granted permission to an online photo editor(the client) to access photos stored on your Google Drive(authorization server) by using the `Login with Google` feature in that online service. By doing so, you are autorized the service to access your photos in Drive without sharing your credentials.<br />
Thus, in effect You *“delegated”* the responsibility of authorizing access to your resources(your photos) to the Google Drive (actually it's, *accounts.google.com*) server (Authorization server). This is called *“Delegated Authorization”*.

In above example, the OAuth has been used in a specific way. Protocol's specification allows developers to use this in multiple ways. We are going take a look at them later.

First let's go through some Oauth terminologies, <br />
- Resource
  : Your Photos in Drive
- Resource Owner
  : You
- Client
  : The online photo editor app
- Authorization Server
  : accounts.google.com server
- Autorization Grant
  : authorization code received from the authorization server
- 