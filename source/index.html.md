---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - android
  - iOS

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Engage SDK API! You can use our API to access Kittn API endpoints, which can get information on various cats, kittens, and breeds in our database.

We have language bindings in Android and iOS! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.


# initialize

> To initialize, use this code:

```java
 EngageConfig engageConfig = new EngageConfig(getApplication(), "region","yourapplicationid","yourclientsecret","userid");
            EngageClient.getInstance().initialize(engageConfig, new EngageResponseListener() {
                @Override
                public void onSuccess(EngageResponse engageResponse) {
                   //perform your action on success
                }

                @Override
                public void onFailure(EngageFailResponse engageFailResponse) {
                  //perform your action on failure
                }
            });
```

> Make sure to replace `region`,`yourapplicationid`, `yourclientsecret` and `userid` with your details.

Initialization API allows you to initialize with the Engage sdk. You can register your application with your application instance, region, application id, client secret and user id.

# sendMetrics

Invoke this api to send the metric code to the engage server

```java
   EngageClient.getInstance().sendMetrics("yourmetriccode");
```

> Make sure to replace `yourmetriccode` with the right metric code.

# Features

## getFeatures

Invoke this api to get all features

```java
     EngageClient.getInstance().getFeatures(new EngageResponseListener() {
            @Override
            public void onSuccess(EngageResponse engageResponse) {
                //perform your action on success
            }

            @Override
            public void onFailure(EngageFailResponse engageFailResponse) {
                //perform your action on failure
            }
        });
```

## isFeatureEnabled

Invoke this api to check if a feature is enabled

```java
    EngageClient.getInstance().isFeatureEnabled(featureCode, new EngageResponseListener() {
            @Override
            public void onSuccess(EngageResponse engageResponse) {

              
            }

            @Override
            public void onFailure(EngageFailResponse engageFailResponse) {
             
            }
        });
```
> Make sure to replace `featureCode` with the right feature code.


## getVariableForFeature

Invoke this api to get a variable associated with this feature

```java
    EngageClient.getInstance().getVariableForFeature("featureCode","variableCode");
```
> Make sure to replace `featureCode` and `variableCode` with the right values.


<aside class="success">
Remember — Engage makes your life easy!
</aside>