# General

The conventions described in this section are http specific.

## Summarizing http labels

### Justification

Http calls are generally fully described by Spans. By adding labels
to http metrics it allows for finely tuned aggregation on those metrics.

### Convention

Below are the labels that should be added to http metrics if they exist on the span.
The label's name should be prefixed with `http`, such as `http.url`.

#### url

The url of the request.

key: `http.url`

example:
`key: http.url`
`value: https://opentelemetry.io/`

#### method

The http method of the request, such as GET, PUT, DELETE, etc.

key: `http.method`

example:
`key: http.method`
`value: GET`

#### status

The status of the response. The value of this label must be a valid Span [`StatusCanonicalCode`](../../trace/api.md#statuscanonicalcode).

key: `http.status`

example:
`key: http.status`
`value: OK`