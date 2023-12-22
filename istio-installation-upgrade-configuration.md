# Istio installation, upgrade and configuration

## Istio installation

Ref: <https://istio.io/latest/docs/setup/install/>

### Install with Istioctl

Ref: <https://istio.io/latest/docs/setup/install/istioctl/>

The simplest option is to install the default Istio configuration profile using the following command:

```shell
istioctl install
```

This command installs the default profile on the cluster defined by your Kubernetes configuration.

#### Install different profiles

You can display the names of Istio configuration profiles that are accessible to istioctl by using this command:

```shell
istioctl profile list
```

For example, the following command can be used to install the `demo` profile:

```shell
istioctl install --set profile=demo
```

#### Check what’s installed

```shell
kubectl -n istio-system get deploy
```

#### Display the configuration of a profile

For example, to view the setting for the demo profile run the following command:

```shell
istioctl profile dump demo
```

To view a subset of the entire configuration, you can use the `--config-path` flag, which selects only the portion of the configuration under the given path:

```shell
istioctl profile dump --config-path components.pilot demo
```

### Install with Helm

### Istio Operator Install
