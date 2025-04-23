# Helm Charts Mirror for Elastic

This repository serves as a **mirror** (clone) of the official Elastic Helm repository (https://helm.elastic.co/) to work around intermittent `403 Forbidden` errors when accessing the upstream.

## Purpose

Due to occasional access restrictions on the official Elastic Helm endpoint, all Helm charts from `https://helm.elastic.co` are mirrored here and published via GitHub Pages.

## Adding this repository to Helm

Use the following commands to add this mirror and update your local Helm cache:

```bash
helm repo add elastic-eck https://pbardov.github.io/helm-eck/repo/elastic
helm repo update
```

You can choose any alias instead of `elastic-eck` (for example, `elastic-mirror`), but be consistent when installing charts.

## Searching and Installing Charts

After adding the repo, list available charts:

```bash
helm search repo elastic-eck
```

Install a chart, for example Elasticsearch:

```bash
helm install my-elasticsearch elastic-eck/elasticsearch --version <version>
```

## Original Source

This mirror is based on the official Elastic Helm repository:

- Official Elastic Helm: https://helm.elastic.co/

---

*Maintained by [pbardov](https://github.com/pbardov). Feel free to open issues or pull requests if you encounter any problems.*

