# Kube-Notes-Infra
<div align="center">
  <img src="images/background-photo.png" alt="K8 Logo" width="75%"/>
  <br><br>
</div>

This is a repository that contains Kubernetes Manifests or [K8s](https://kubernetes.io/) for a distributed web application.
The distributed application functions as a note-taking service with custom authentication.

The overall project is composed of the following microservices:
 - **React-Frontend**: This is the client facing front-end web application, it is powered by React and Vite | [GitHub Repo](https://github.com/shahLLL/Kube-Notes-FrontEnd) | [DockerHub Repo](https://hub.docker.com/repository/docker/shahlll/kube-notes-frontend)
 - **Notes-Service**: This is the Node Service that handles logic pertaining to creating, destroying, adding, and updating Notes | [GitHub Repo](https://github.com/shahLLL/Kube-Notes-Notes) | [DockerHub Repo](https://hub.docker.com/repository/docker/shahlll/kube-notes-notes/general)
 - **Auth-Service**: This is the Node Service that handles custom user authentication  | [GitHub Repo](https://github.com/shahLLL/Kube-Notes-Auth) | [DockerHub Repo](https://hub.docker.com/repository/docker/shahlll/kube-notes-auth/general)
 - **PostgreSQL**: This is a Relational Database that is used to store user information and enable authentication & authorization | [Official Website](https://www.postgresql.org/)
 - **MongoDB**: This is a NOSQL Database used to store Notes Data | [Official Website](https://www.mongodb.com/)
 - **Redis**: This is a Caching Layer used to speed up Notes Query | [Official Website](https://redis.io/)

 This project can be deployed in any Kubernetes environment. **ConfigMaps**, **Deployments**, and **Services** have been separated into their own folders. This project does use **Secret** values and would need to be manually configured by the user. Please consult [this](https://kubernetes.io/docs/concepts/configuration/secret/) resource to learn how. The **Secret** values are as follows:

 ```
 SECRET_NAME; SECRET_KEY
 postgres-credentials;password -> Password required for PostgreSQL Database
 auth-secrets; jwt-secret -> Secret String required to enable Authentication & Authorization
 ```

Contributions and feedback are more than welcomed. 

When contributing to this project or using it in any way, please do pay attention to: [LICENSE](https://github.com/shahLLL/Kube-Notes-Infra/tree/main?tab=Apache-2.0-1-ov-file)

☕☕☕**CHEERS AND THANK YOU**☕☕☕






