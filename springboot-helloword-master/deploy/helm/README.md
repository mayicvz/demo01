## deploy helm chart to assetforce namespace
helm upgrade -f values-poc.yaml -i -n assetforce assetforce ./

## show helm render result
helm install -f values-poc.yaml --dry-run --debug -n assetforce assetforce ./

## deploy app for zone2
helm upgrade -f values-poc.yaml -i -n assetforce assetforce-zone2 --set assetforce.core.zoneName=zone2 --set assetforce.core.isDefaultZone=false ./
