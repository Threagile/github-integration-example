# github-integration-example

Example of how to integrate Threagile into GitHub workflows:

This repo acts as some sort of template to see the integration of Threagile into a GitHub workflow in action.
Usually here would be a real project with real source and other stuff. Also such a repo contains a **threagile.yaml** file, which contains the threat model input (see the Threagile docs for info about this).
*Here we're using the Threagile example YAML file as an example threat model input.*

## GitHub Workflow Integration
This example repo has a GitHub workflow associated, which executes a job once the Threagile model file (threagile.yaml) changes on a push (see the [.github/workflows/main.yaml](.github/workflows/main.yaml) file for this).


This workflow executes the *run-threagile-action* (published on the GitHub action's marketplace as open-source) to work on the threagile.yaml threat model file and generate the data-flow-diagram (DFD), threat model report (PDF), Excel and JSON exports, etc. on every change of threagile.yaml. The full set of generated results are preserved as the action's artifcats (see the actions tab). Additionally the data-flow-diagram and threat model report are also pushed to the repo (in the folder threagile/output) for further automatic referencing from within this README.md (or any other markdown file) in the repo.

*See below... ;)*



## Threat Model Analysis
The open-source toolkit for agile threat modeling, Threagile, was used to model and analyze potential threats.

### Data-Flow Diagram (DFD)
The following DFD was generated by Threagile during threat model analysis:
![Data-Flow Diagram (DFD)](/threagile/output/data-flow-diagram.png?raw=true "Data-Flow Diagram (DFD)")

### Threat Model Report
The following report was generated by Threagile during threat model analysis:
[Threat Model Report](/threagile/output/report.pdf?raw=true)

