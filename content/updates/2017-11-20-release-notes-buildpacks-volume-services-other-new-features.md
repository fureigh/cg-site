+++
date = "2017-11-20"
title = "cloud.gov monthly update: Buildpack notifications, volume services, and other new features"
+++
We’ve been hard at work shipping out new features to help you make your apps better, more secure, and improve your experience developing and deploying them. There’s a lot more in here than usual. We hope you see some features and additions in here that you’ve been waiting for. As always, get in touch with us if you have any questions or feedback about these features. See you next month.

### Added

* Part of keeping your app on cloud.gov secure is [using the latest version of your app’s buildpack]({{< relref "docs/getting-started/app-maintenance.md" >}}). In addition to keeping you updated in these release notes, we’ll now send you an email notification when a new version of your buildpack is available.
* We have experimental support for [volume services]({{< relref "docs/apps/experimental/volume-services.md" >}}). Since a cloud.gov app normally has a short-lived file system, this enables you to build an app that requires persistent file storage. [Contact us if you’d like to try this]({{< relref "docs/apps/experimental/volume-services.md#how-to-use-this-service" >}}).
* One of our engineers gave us the ability to make [Mermaid diagrams](https://mermaidjs.github.io/) on the cloud.gov website, and we almost got carried away creating visualizations of different parts of the platform. Here are a couple we think will help you out:
  * [A comparison of how apps with custom domains and those with the default \*.app.cloud.gov domain are served to users]({{< relref "docs/apps/custom-domains.md#comparison-of-default-domains-and-custom-domains" >}}).
  * [How to incorporate a CI/CD workflow into your app]({{< relref "docs/apps/continuous-deployment.md#configure-your-service" >}}).
* [The cloud.gov dashboard](https://dashboard.fr.cloud.gov/) now lets you manage environment variables for your apps. To see it in action, go to an app page in the dashboard and try viewing, adding, or editing an environment variable. You can also see all the environment variables set by the system from the same view.

<img src="/img/dashboard-envs.png" alt="Screenshot of the environment variable editing view on the dashboard" style="border:1px solid grey;" />

### Updates

Make sure to use the latest version of the Cloud Foundry CLI. The most recent updates contain new commands and bug fixes. You can [download the latest binary for Windows, Mac, or Linux from GitHub](https://github.com/cloudfoundry/cli/releases).

### Announcement

We will not, as we previously announced, be [switching users with cloud.gov accounts to sign in with MAX.gov]({{< relref "updates/2017-08-21-max-gov-migration-instructions.md" >}}).

### Coming soon

#### Sandboxes will expire after 90 days

We plan to automatically delete apps in [sandbox spaces]({{< relref "overview/pricing/free-limited-sandbox.md#sandbox-limitations" >}}) after 90 days. We’ll send email notifications before this happens. If you’re developing something you need to keep long-term, we recommend moving it to a prototyping space. If you’d like to [start the process of purchasing a prototyping package]({{< relref "overview/pricing/prototyping.md" >}}), get in touch with us.

#### Additional TIC compliance support

To support agency implementations of Trusted Internet Connection (TIC) requirements, we’ve published [documentation about complying with TIC for apps on cloud.gov]({{< relref "docs/compliance/meeting-tic-requirements.md" >}}). To support a wider range of agency TIC needs, we’ve also built a way to [support restricting users to trusted IP ranges]({{< relref "docs/apps/experimental/restricting-users-to-trusted-ip-ranges.md" >}}). We’re waiting to fully implement it until after it’s passed FedRAMP review, but in the meantime, let us know if you have questions or want to use it.

### Platform releases

We upgraded the Cloud Foundry deployment to [v278](https://github.com/cloudfoundry/cf-release/releases/tag/v278).

You should [restage your application](https://cloud.gov/docs/getting-started/app-maintenance/) to [incorporate fixes in the base filesystem](https://docs.cloudfoundry.org/devguide/deploy-apps/stacks.html#cli-commands) and ensure you’re running the most recent language version supported by your [buildpack](https://docs.cloudfoundry.org/buildpacks/).

#### Additional upgrades
* [Diego v1.29.2](https://github.com/cloudfoundry/diego-release/releases/tag/v1.29.2)
* [Stemcell v3468.5](https://bosh.io/stemcells/bosh-aws-xen-hvm-ubuntu-trusty-go_agent)
* Buildpacks:
  * [Staticfile v1.4.18](https://github.com/cloudfoundry/staticfile-buildpack/releases/tag/v1.4.18)
  * [Java v4.6](https://github.com/cloudfoundry/java-buildpack/releases/tag/v4.6)
  * [Ruby v1.7.5](https://github.com/cloudfoundry/ruby-buildpack/releases/tag/v1.7.5)
  * [NodeJS v1.6.10](https://github.com/cloudfoundry/nodejs-buildpack/releases/tag/v1.6.10)
  * [Go v1.8.13](https://github.com/cloudfoundry/go-buildpack/releases/tag/v1.8.13)
  * [Python v1.6.1](https://github.com/cloudfoundry/python-buildpack/releases/tag/v1.6.1)
  * [PHP v4.3.43](https://github.com/cloudfoundry/php-buildpack/releases/tag/v4.3.43)
  * [.NET-core v1.0.30](https://github.com/cloudfoundry/dotnet-core-buildpack/releases/tag/v1.0.30)
  * [Binary v1.0.15](https://github.com/cloudfoundry/binary-buildpack/releases/tag/v1.0.15)