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
[https://projects.eclipse.org/projects/iot.aerios](https://projects.eclipse.org/projects/iot.aerios)

📦 Resources portal (GitHub Pages):  
[https://eclipse-aerios.github.io/resources](https://eclipse-aerios.github.io/resources)

💻 GitHub repository:   
[https://github.com/eclipse-aerios](https://github.com/eclipse-aerios)

🐳 Docker Hub repository:  
[https://hub.docker.com/u/eclipseaerios](https://hub.docker.com/u/eclipseaerios)

☸️ Helm chart repository:  
[https://eclipse-aerios.github.io/resources/charts](https://eclipse-aerios.github.io/resources/charts)

☸️ Artifact Hub repository:  
[https://artifacthub.io/packages/search?org=eclipse-aerios](https://artifacthub.io/packages/search?org=eclipse-aerios)


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

### How to add or update Helm charts

After adding the already packaged Helm charts inside the [charts](./charts/) folder, run the following command to update the context of the [index.yaml](./charts/index.yaml) file:

```bash
helm repo index charts --url https://eclipse-aerios.github.io/resources/charts --merge .\charts\index.yaml --debug
```

Then, commit and push the changes.

### How to use

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

## 🐳 Docker Compose files repository

To download a Docker Compose file:

```bash
wget https://raw.githubusercontent.com/eclipse-aerios/resources/refs/heads/main/docker-compose/<component>/docker-compose.yaml
```

For instance:

```bash
wget https://raw.githubusercontent.com/eclipse-aerios/resources/refs/heads/main/docker-compose/federator/docker-compose.yaml
```

To quickly download and start a Docker Compose deployment with no modifications:

```bash
curl https://raw.githubusercontent.com/eclipse-aerios/resources/refs/heads/main/docker-compose/<component>/docker-compose.yaml | docker compose -f /dev/stdin up -d
```

For instance:

```bash
curl https://raw.githubusercontent.com/eclipse-aerios/resources/refs/heads/main/docker-compose/federator/docker-compose.yaml | docker compose -f /dev/stdin up -d
```