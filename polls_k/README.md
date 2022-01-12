# Manifest for kustomization

## Usage

### Build manifest

```bash
kubectl kustomize overlays/development/
```

### Build manifest and apply to cluster

Make sure you are in the correct context! THe namespace `"polls"` must exist, so you may have to create it:

```bash
kubectl create ns polls
```
Then you can build the manifest for the development environment:
```bash
kubectl kustomize overlays/development/ | kubectl apply -f -
```
