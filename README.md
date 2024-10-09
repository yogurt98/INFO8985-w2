# INFO8995-telemetry
run open telemetry demo in codespace

TLDR;

```
pip install -r requirements.txt
ansible-playbook playbook.yml
kubectl port-forward svc/my-otel-demo-frontendproxy 8080:8080
```

If you need to delete a cluster and start over you can run:

```
k3d cluster delete local-k8s
rm -rf ~/.kube
```

Then you can take it from the top.

Note: This also works (faster) in vscode local with docker desktop installed. 

1. From the command palette `Dev Containers: Clone Repository in Container Volume`. 

2. Choose this repository `https://github.com/rhildred/INFO8985-telemetry.git`. 

3. Follow the steps from TLDR;

The deliverable for the lab is to follow the instructions in chapter 4 of the text and note your observations in a markdown file.

There is a lot happening in this lab. Please look at the [helm chart](https://github.com/open-telemetry/opentelemetry-helm-charts/blob/main/charts/opentelemetry-demo/values.yaml). Pay special attention to the components and think of how they would appear in a deployment diagram. This distributed system has a few different pieces, telemetry allows us to view the system as a whole.