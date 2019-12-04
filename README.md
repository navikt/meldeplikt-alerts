# meldeplikt-alerts
Lager alerts for appene til team meldeplikt

For mer informasjon om hvordan alarmene fungere se: `https://doc.nais.io/observability/alerts`

## For NAV ansatte
Vi er tilgjenngelig på slack kanalen #meldekort

## Komme i gang
En kan bruke `https://prometheus.nais.preprod.local/graph` som hjelp til å teste queries.

Deploy alert i ønsket cluster: `kubectl apply -f meldekortservice-alerts.yaml`

Om alerten allerede finnes må den fjernes først: `kubectl delete alert meldekortservice-alerts`

Triggede alerts dukker opp i #meldekort-alerts på Slack.
