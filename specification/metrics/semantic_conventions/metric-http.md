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

The url of the request. Note that parameterized urls can lead to high cardinality
which is why urls should follow the same convention as
[http span names](../../trace/semantic_conventions/http.md#name).

key: `http.url`

example: `http.url: https://opentelemetry.io/`

#### method

The http method of the request, such as GET, PUT, DELETE, etc.

key: `http.method`

example: `http.method: GET`

#### status

The status of the response. The value of this label must be a valid Span
[`StatusCanonicalCode`](../../trace/api.md#statuscanonicalcode).

key: `status`

In order to match other non-http labels `http` is omitted from the status label key.

example: `status: OK`