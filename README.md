# docker-gitlab

# How Install Documents :

1. Download File at :

https://github.com/AshkanSecure/docker-gitlab.git

2. insert Command :

docker-compose -f docker-compose.yml up


# How Install Video Learning :

https://www.youtube.com/watch?v=JvM8bO1ywvE&


# **How backup container:**

1. Commit the required container as an image

`docker commit -p [container-id] backup01`


2. You can save the image backup01 to tar file using the following command:


`docker save -o backup01.tar backup01`

`ls -al | grep back
-rw------- 1 root root 178697728 Mar 31 23:35 backup01.tar`

You may choose to save the tar file on NFS mount point. Another option is directly pushing the image backup01 to your local registry. Before pushing the backup image, we need to tag it appropriately.


`docker tag backup01 localhost:5000/backup-image:v1`

In this example, localhost is the hostname where the local registry is located and 5000 is the port number that the registry listens on. If you are working on a Docker engine located on a different host to the registry, you must change the hostname to point to the correct host. Note the repository and tag name, backup-image:v1 in the example, must all be in lower case to be a valid tag.

`docker push backup-image:v1`



## Donate

Want to keep this project going? Please donate generously [https://www.buymeacoffee.com/securemanager](https://www.buymeacoffee.com/securemanager)

[![Build](https://www.buymeacoffee.com/assets/img/custom_images/yellow_img.png)](https://www.buymeacoffee.com/securemanager)

