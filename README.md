# intelligent-tekton-pipeline-app

Intelligent Pipelines: Bringing AI/ML into DevSecOps Automation.

## Overview

`intelligent-tekton-pipeline-app` is the application-side companion repository of
the Intelligent Pipelines project. The idea behind the project is to bring
AI/ML assistance into DevSecOps automation built on Tekton pipelines running on
OpenShift: instead of operators digging through pipeline runs by hand, intelligent
tooling surfaces what ran, what failed, and why, so failures can be understood
and fixed faster.

This repository is the home planned for the application component of that idea.
It sits alongside two sibling repositories:

- [`intelligent-tekton-pipelines`](https://github.com/psehgaft/intelligent-tekton-pipelines)
  — the project overview and concept.
- [`inteligent-pipelines-llamastack`](https://github.com/psehgaft/inteligent-pipelines-llamastack)
  — the MCP server that exposes Tekton pipeline data (pipelines, pipeline runs,
  task runs, and failed task logs) from an OpenShift cluster to AI assistants.

## Current status

This repository currently contains only this overview. There is no application
code, pipeline definition, or runnable component here yet — the working piece of
the project today is the MCP server in `inteligent-pipelines-llamastack`. Treat
everything below under "Planned directions" as goals, not shipped functionality.

## Planned directions

- An application that consumes pipeline intelligence (runs, failures, logs) and
  presents it in a form operators can act on.
- AI-assisted triage of failed pipeline runs, building on the data exposed by
  the MCP server.
- Integration with the Tekton/OpenShift workflows described in the sibling
  repositories.

## Prerequisites

To follow the project as a whole, you need:

- An OpenShift cluster with Tekton Pipelines installed (for the MCP server
  sibling repository).
- The `oc` CLI, authenticated against that cluster.
- Python 3, for running the MCP server.

This repository itself has no prerequisites yet, because it contains no code.

## Getting started

1. Start with the project overview in
   [`intelligent-tekton-pipelines`](https://github.com/psehgaft/intelligent-tekton-pipelines).
2. To see the working component, follow the setup instructions in
   [`inteligent-pipelines-llamastack`](https://github.com/psehgaft/inteligent-pipelines-llamastack)
   to build and run the Tekton MCP server against your cluster.
3. Watch this repository for the application component as it lands.

## Repository layout

```text
LICENSE    GNU General Public License v2
README.md  This file
```

## License

This project is licensed under the GNU General Public License v2 — see the
[`LICENSE`](LICENSE) file for the full text.
