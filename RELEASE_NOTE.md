# Release note

## 2020-07-21

### 💫 New Features

 - [AWS Support](https://github.com/staroids/community/issues/2) 

    Now you can choose AWS region when creating SKE!

    ![](https://user-images.githubusercontent.com/63678710/88068484-1ed93000-cb25-11ea-8810-16e793a53e85.png)

## 2020-07-20

### 💫 New Features

 - `starctl` Command line interface

   `starctl` CLI is released and available as an open-source. `starctl` helps you programmatically access staroid features, including access Kubernetes API from your machine.

   Check https://github.com/staroids/starctl

 - API access token

   You can now generate/revoke API token from [Access Tokens](https://staroid.com/settings/accesstokens) menu. Access token can be used for

    - staroid REST API
    - starctl CLI
    - get access to your application end point deployed in SKE

## 2020-07-09

### 🛸 Enhancements

CI build system upgraded [Skaffold](https://skaffold.dev/) version from v1.7.0 to v1.12.0. 😀

## 2020-07-07

### 💫 New Features

  ![](https://user-images.githubusercontent.com/1540981/87073386-2a962f80-c1d2-11ea-8977-61f323f7c7c7.png)

  - Spot instance

    Pod can be located in Spot instance to reduce cost by simply adding `pod.staroid.com/spot: true` label.

    See https://docs.staroid.com/ske/pod.html#pod for more details.

  - Dedicated node

    Pod can be located in Dedicated VM instance for higher IO throughput by simply adding `pod.staroid.com/isolation: dedicated` label.

    See https://docs.staroid.com/ske/pod.html#pod for more details.


## 2020-06-30

### 🛸 Enhancements
  - Increased Test Drive namespace resource quota
    
    Namespace resource quota for TestDrive for free tier is increased from

    | Quota | Before | After |
    | ----- | ------ | ----- |
    | max namespace cpu request | 4 | 8 |
    | max namespace memory request | 4Gi | 8Gi |
    | max namespace cpu limit | 8 | 16 |
    | max namespace memory limit | 8Gi | 32Gi |

    Note that, this quota is only for TestDrive. Your normal Virtual Cloud quota is unlimited.


## 2020-06-29

### 🛸 Enhancements

  - Terminal is now moved into the Instance view from Virtual cloud view with the name 'shell'. Now user can manage it (start/stop).

  ![](https://user-images.githubusercontent.com/1540981/86165701-87a22f00-bac8-11ea-8c42-541480a9e312.png)

  - Connecting Log console (and Shell) takes now a much short time. From 5-15 seconds to around 1 second! 🚀

### 🐛 Bug Fixes

  - Projects listed in the Universe show the wrong community rate.
  - Fixed Log console and Terminal shows connection closed very frequently. 😀

  ![](https://user-images.githubusercontent.com/1540981/86163432-12812a80-bac5-11ea-9310-1bcbfa244cf4.png)

## 2020-06-20

### 💫 New Features

  - Now you can browse ['nfs' type Persistent Volume Claim](https://docs.staroid.com/virtual_cloud/storage.html#storageclassname) from the web interface.

    ![](https://user-images.githubusercontent.com/1540981/86165680-7f49f400-bac8-11ea-8885-53d97b77c4af.png)

    We used https://github.com/coderaiser/cloudcmd to run the browser. Thank the Cloud Commander community!

## 2020-06-18

### 💫 New Features

  - Update existing instance!

    ![](https://user-images.githubusercontent.com/1540981/86165633-6f321480-bac8-11ea-938c-8b38ffd23b48.png)

    Now you can change configurations or upgrade to a new version.


## 2020-05-11

### 💫 New Features

  - Now you can stop and restart the instance. [issue#5](https://github.com/staroids/community/issues/5).

    ![](https://user-images.githubusercontent.com/63678710/81838258-bce3c500-94fa-11ea-9cdf-06d05bc3c039.png)

    Stop terminates all running Pods but keeps ConfigMaps, Secrets, and PersistentVolumeClaim.

  - Allow public access to the instance. [issue#6](https://github.com/staroids/community/issues/6).

    ![](https://user-images.githubusercontent.com/63678710/84688011-6f8cb600-aef3-11ea-842d-8304d8cfffb5.png)

    With this, you can deploy an instance that provides a service to the public internet.
