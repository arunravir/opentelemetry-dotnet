# Changelog

## Unreleased

* Moving Jaeger Process from public to internal.
  ([#1421](https://github.com/open-telemetry/opentelemetry-dotnet/pull/1421))

## 0.7.0-beta.1

Released 2020-Oct-16

* Renamed `MaxPacketSize` -> `MaxPayloadSizeInBytes` on `JaegerExporterOptions`.
  Lowered the default value from 65,000 to 4096.
  ([#1247](https://github.com/open-telemetry/opentelemetry-dotnet/pull/1274))

## 0.6.0-beta.1

Released 2020-Sep-15

* Removed `MaxFlushInterval` from `JaegerExporterOptions`. Batching is now
  handled  by `BatchExportActivityProcessor` exclusively.
  ([#1254](https://github.com/open-telemetry/opentelemetry-dotnet/pull/1254))

## 0.5.0-beta.2

Released 2020-08-28

* Changed `JaegerExporter` to use `BatchExportActivityProcessor` by default
  ([#1125](https://github.com/open-telemetry/opentelemetry-dotnet/pull/1125))
* Span links will now be sent as `FOLLOWS_FROM` reference type. Previously they
  were sent as `CHILD_OF`.
  ([#970](https://github.com/open-telemetry/opentelemetry-dotnet/pull/970))
* Fixed issue when span has both the `net.peer.name` and `net.peer.port`
  attributes but did not include `net.peer.port` in the `peer.service` field
  ([#1195](https://github.com/open-telemetry/opentelemetry-dotnet/pull/1195)).

* Renamed extension method from `UseJaegerExporter` to `AddJaegerExporter`.

## 0.4.0-beta.2

Released 2020-07-24

* First beta release

## 0.3.0-beta

Released 2020-07-23

* Initial release
