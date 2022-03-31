# Problem Statements

1. Check kubectl installation (find its version) and access to cluster. How many nodes/ pods/ deployments/ services/ configmaps/ secrets/ serviceaccounts/ roles are there ?
2. Beginner exercise: do the challenges in [01-pods-deployments.md](01-pods-deployments.md)
3. Beginner exercise (optional): do the challenges in [02-service-discovery-and-loadbalancing.md](02-service-discovery-and-loadbalancing.md)
4. Create nginx deployment with 3 replicas. Expose via a service of type load balancer and check you can access it from the web browser.
5. modify the deployment to attach an empty directory as a volume and mount it at the document root `/usr/share/nginx/html`. What happens when you access the service endpoint now ?
6. A an init container or side-car container with the shared volume and set it up to create an index.html with message "Hello from <your team name>"
7. Access via web-browser and check if this new index.html is served.
8. modify the init container to also append pod name and IP address to the index.html contents. How does this affect the service ?
9. extend the init container to also list all deployments in all namespaces and append this to the index.html page. Use the default serviceaccount for this purpose.
10. modify the deployment to create an empty config-map on startup with same name as the pod (1 for each pod). Does the defauly service account accomplish this ?
11. Create a new service account and bind it to a role that has ability to create, edit and delete configmaps
12. associate the deployment with this service account and modify to populate the configmap with the pod name and ip address.
12. What happens when you scale the deployment now ?
