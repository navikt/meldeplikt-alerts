[![Build status](https://github.com/navikt/meldeplikt-alerts/workflows/Deploy%20alerts%20to%20all%20environments/badge.svg)](https://github.com/navikt/meldeplikt-alerts/workflows/Deploy%20alerts%20to%20all%20environments/badge.svg)

# meldeplikt-alerts
Lager alerts for Team meldeplikt sine applikasjoner.

For mer informasjon om hvordan alarmene fungerer se: `https://doc.nais.io/observability/alerts`.

## Utvikling
Generelle alerts for alle miljø legges i `alerts-common.yaml` mens alerts for et gitt cluster eller applikasjon legges i `alerts-<cluster>>.yaml`.
Ved deploy merges generelle alerts og cluster-spesifikke alerts sammen i en fil.

    .
    ├── ...
    ├── .nais
    │   ├── alerts-common.yaml   # Felles alerts
    │   ├── alerts-fss.yaml      # Alerts for applikasjoner i FSS
    │   └── alerts-gcp.yaml      # Alerts for applikasjoner i GCP
    └── ...

## Deploy
Endring på utviklingsbranch trigger deploy til dev-fss og dev-gcp.
Endring på master-branch trigger deploy til alle miljø.

## Oppfølging
Triggede alerts dukker opp i #team-meldeplikt-alerts på Slack.

## For NAV ansatte
Vi er tilgjengelig på Slack i kanalen #team-meldeplikt.
