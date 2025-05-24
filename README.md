# terraform

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/terraform)
[![General Workflow](https://github.com/rolehippie/terraform/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/terraform/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/terraform/actions/workflows/docs.yml/badge.svg)](https://github.com/rolehippie/terraform/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/rolehippie/terraform/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/terraform/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/terraform)](https://github.com/rolehippie/terraform/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.terraform-blue)](https://galaxy.ansible.com/rolehippie/terraform)

Ansible role to install terraform infrastructure as code tool.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [terraform_arch](#terraform_arch)
  - [terraform_checkov_enabled](#terraform_checkov_enabled)
  - [terraform_checkov_version](#terraform_checkov_version)
  - [terraform_install_path](#terraform_install_path)
  - [terraform_keyring](#terraform_keyring)
  - [terraform_tflint_arch](#terraform_tflint_arch)
  - [terraform_tflint_download](#terraform_tflint_download)
  - [terraform_tflint_enabled](#terraform_tflint_enabled)
  - [terraform_tflint_version](#terraform_tflint_version)
  - [terraform_tfsec_arch](#terraform_tfsec_arch)
  - [terraform_tfsec_download](#terraform_tfsec_download)
  - [terraform_tfsec_enabled](#terraform_tfsec_enabled)
  - [terraform_tfsec_version](#terraform_tfsec_version)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`

## Default Variables

### terraform_arch

Architecture for terraform repo

#### Default value

```YAML
terraform_arch: "{{ 'arm64' if ansible_architecture == 'aarch64' else 'amd64' }}"
```

### terraform_checkov_enabled

Enable installation of checkov

#### Default value

```YAML
terraform_checkov_enabled: false
```

### terraform_checkov_version

Define a specific version of checkov

#### Default value

```YAML
terraform_checkov_version: 2.3.214
```

### terraform_install_path

Path to install the binaries

#### Default value

```YAML
terraform_install_path: /usr/bin
```

### terraform_keyring

Path for the repository keyring

#### Default value

```YAML
terraform_keyring: /usr/share/keyrings/hashicorp-archive-keyring.gpg
```

### terraform_tflint_arch

Architecture for tflint

#### Default value

```YAML
terraform_tflint_arch: "{{ 'arm64' if ansible_architecture == 'aarch64' else 'amd64'
  }}"
```

### terraform_tflint_download

URL to download tflint from

#### Default value

```YAML
terraform_tflint_download: https://github.com/terraform-linters/tflint/releases/download/v{{
  terraform_tflint_version }}/tflint_linux_{{ terraform_tflint_arch }}.zip
```

### terraform_tflint_enabled

Enable installation of tflint

#### Default value

```YAML
terraform_tflint_enabled: true
```

### terraform_tflint_version

Version of tflint to install

#### Default value

```YAML
terraform_tflint_version: 0.58.0
```

### terraform_tfsec_arch

Architecture for tfsec

#### Default value

```YAML
terraform_tfsec_arch: "{{ 'arm64' if ansible_architecture == 'aarch64' else 'amd64'
  }}"
```

### terraform_tfsec_download

URL to download tfsec from

#### Default value

```YAML
terraform_tfsec_download: https://github.com/aquasecurity/tfsec/releases/download/v{{
  terraform_tfsec_version }}/tfsec_{{ terraform_tfsec_version }}_linux_{{ terraform_tfsec_arch
  }}.tar.gz
```

### terraform_tfsec_enabled

Enable installation of tfsec

#### Default value

```YAML
terraform_tfsec_enabled: true
```

### terraform_tfsec_version

Version of tfsec to install

#### Default value

```YAML
terraform_tfsec_version: 1.28.14
```

## Discovered Tags

**_terraform_**


## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
