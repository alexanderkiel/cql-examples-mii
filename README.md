# MII CQL Examples

This repository contains example CQL queries from the [German Research Data Portal for Health][1].

## Execute Queries

First you need to install the command line tool [blazectl][2] and optionally [jq][4]. After that, you need to run a
[Blaze FHIR server][3]. In our examples the Blaze FHIR server is reachable under `http://localhost:8080/fhir`.

### Diabetes Mellitus

```sh
blazectl --server http://localhost:8080/fhir evaluate-measure queries/diabetes-mellitus.yml | jq -f result.jq
```

### CT Scan

```sh
blazectl --server http://localhost:8080/fhir evaluate-measure queries/ct-scan.yml | jq -f result.jq
```

### Hemoglobin

```sh
blazectl --server http://localhost:8080/fhir evaluate-measure queries/hemoglobin.yml | jq -f result.jq
```

[1]: <https://forschen-fuer-gesundheit.de>
[2]: <https://github.com/samply/blazectl>
[3]: <https://github.com/samply/blaze>
[4]: <https://jqlang.github.io/jq/>
