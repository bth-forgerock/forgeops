# ForgeRock DevOps and Cloud Deployment

_Kubernetes deployment for the ForgeRock&reg; Identity Platform._

This repository provides Docker and Kustomize artifacts for deploying the 
ForgeRock Identity Platform on a Kubernetes cluster. 

This GitHub repository is a read-only mirror of
ForgeRock's [Bitbucket Server repository](https://stash.forgerock.org/projects/CLOUD/repos/forgeops). 
Users with ForgeRock BackStage accounts can make pull requests on our Bitbucket 
Server repository. ForgeRock does not accept pull requests on GitHub.

## Disclaimer

>This repository is provided on an “as is” basis, without warranty of any kind, 
to the fullest extent permitted by law. ForgeRock does not warrant or guarantee 
the individual success developers may have in implementing the code on their
development platforms or in production configurations. ForgeRock does not 
warrant, guarantee or make any representations regarding the use, results of use,
accuracy, timeliness or completeness of any data or information relating to these 
samples. ForgeRock disclaims all warranties, expressed or implied, and in 
particular, disclaims all warranties of merchantability, and warranties related
to the code, or any service or software related thereto. ForgeRock shall not be
liable for any direct, indirect or consequential damages or costs of any type 
arising out of any action taken by you or others related to the samples.

## How to Work With This Repository

See the instructions [here](https://ea.forgerock.com/docs/forgeops/forgeops.html) for information about how to work with this pre-release software.

>Note: The forgeops repository’s master branch contains pre-release software that is not supported by ForgeRock.

If you want to work with the latest stable forgeops repository release, use the 
[release/7.1.0 branch](https://github.com/ForgeRock/forgeops/tree/release/7.1.0) and use the [corresponding documentation](https://backstage.forgerock.com/docs/forgeops/7.1/index.html).

## What's New?

See the [Devops Release Notes](https://ea.forgerock.com/docs/forgeops/rn/rn.html) to view the new features and changes after May 12, 2021.

## ForgeRock Identity Platform Configuration

The provided configuration, which we call the Cloud Developer's Kit (CDK),
is a basic installation that can be further extended by developers to meet their requirements. 
The configuration provides the following features:

* Deployments for ForgeRock AM, IDM, DS and IG. IG is not deployed by default, but is available optionally.
* AM configured with a single root realm.
* A number of OIDC clients configured for AM/IDM integration and for smoke tests.
Note that the `idm-provisioning`, `idm-admin-ui` and the `end-user-ui` client configurations are required for the
integration of IDM and AM.
* Directory service instances configured for:
   * The shared AM/IDM repo (ds-idrepo).
   * The AM dynamic runtime data store for polices and agents. Currently, the ds-idrepo is used.
   * The Access Manager Core Token Service (ds-cts).
* A Gatling test harness, which exercises the basic deployment and can be modified to include additional tests.


## Getting Started

If you just want to observe the ForgeRock Identity Platform in action on a 
Kubernetes cluster, you can try out our CDK deployment. You'll need to install 
the required third-party software, set up a Kubernetes cluster, and install the 
ForgeRock Identity Platform. 

See the [CDK documentation](https://ea.forgerock.com/docs/forgeops/cdk/overview.html) 
for detailed information about all these tasks.

## Accessing Platform UIs and APIs

Details [here](https://ea.forgerock.com/docs/forgeops/cdk/access.html).

## Managing Configurations

ForgeRock uses the `config.sh` script to manage configurations. See [here](https://ea.forgerock.com/forgeops/cdk/develop/intro.html) for more information.


## Secrets

ForgeRock uses secrets generated by [Secret Agent Operator](https://ea.forgerock.com/forgeops/deployment/security/secret-agent.html).
 

## Troubleshooting Tips

See the [troubleshooting page](https://ea.forgerock.com/docs/forgeops/troubleshooting/overview.html)
in the CDK documentation.

## Cleaning up

See [CDK Shutdown and Removal](https://ea.forgerock.com/docs/forgeops/cdk/shutdown.html)
in the CDK documentation. 