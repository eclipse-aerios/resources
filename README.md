# Eclipse aeriOS – Resources Repository

This repository hosts **deployment and installation resources** for the
[Eclipse aeriOS](https://projects.eclipse.org/projects/iot.aerios) project, including:

- Docker Compose files
- Helm charts
- Installation scripts and configuration examples
- Supporting documentation
- Static files such as images


<p>
  <img src="./images/aeriOS-logo-horizontal.png" alt="aeriOS Logo" width="300"/>
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="./images/eclipse_incubation_vertical.png" alt="aeriOS Logo" width="100"/>
</p>


## 🔗 Documentation & Website

<!-- 📘 Read The Docs documentation:  
https://docs.aerios-project.eu/ -->

🌍 Project website:  
https://projects.eclipse.org/projects/iot.aerios

📦 Resources portal (GitHub Pages):  
https://eclipse-aerios.github.io/resources

💻 GitHub repository:   
https://github.com/eclipse-aerios

🐳 Docker Hub repository:  
https://hub.docker.com/u/eclipseaerios

<!-- ☸️ Artifact Hub repository:  
https://artifacthub.io/packages/search?org=eclipse-aerios -->


## 📂 Repository Structure

```
resources/
├── docker-compose/
│ ├── <component-name>/
│ │ ├── docker-compose.yaml
│ │ ├── config-files.json
├── charts/
│ ├── <components-charts.tgz
│ └── index.yaml
├── docs/
└── images/
```

## ☸️ Helm chart repository

First, add the aeriOS Helm chart repository

```bash
helm repo add eclipse-aerios https://eclipse-aerios.github.io/resources/charts
```

Then, check if the addition of this Helm chart repository has been performed properly by listing all the available charts:

```bash
helm repo update
helm search repo eclipse-aerios
```

Now, Eclipse aeriOS Helm charts can be installed. For instance:

```bash
helm install federator eclipse-aerios/federator --debug
```
