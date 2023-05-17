tequ-node-red-entso-e
=====================

Query electricity spot prices from ENTSO-E Transparency Platform.

## Install

Run the following command in your Node-RED user directory - typically `~/.node-red`

        npm install tequ-node-red-entso-e

## Information

Queries electricity spot prices from ENTSO-E Transparency Platform.

### Inputs

`msg.payload` is used to override parameters configured in Node dialog.

: payload (object) :  JSON object containing one or more query parameters.

Possible parameters in `msg.payload`

: securityToken (string) : API key

: documentType (string) : Document type, Default is `A44`

: in_Domain (string) : In Domain, Default is `10YFI-1--------U`

: out_Domain (string) : Out Domain, Default is `10YFI-1--------U`

: periodStart (string) : Query period start time `202305162100`

: periodEnd (string) : Query period end time `202305172100`


### Outputs

: payload (array) : Spot prices. Array of JSON objects.

Values in JSON object

: ts (string) : Timestamp UTC.

: price (number) : Spot price for timestamp.

### Details

For more information about possible parameter values, please look:

[ENTSO-E API docs](https://transparency.entsoe.eu/content/static_content/Static%20content/web%20api/Guide.html)
