# Changelog
All notable changes to this library will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this library adheres to Rust's notion of
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Unreleased

## [v0.3.6] - 2025-05-20

### Added
- `service.LightdInfo` has added field `donationAddress`
- `service.CompactTxStreamer.GetTaddressTransactions`. This duplicates 
  the `GetTaddressTxids` method, but is more accurately named.

### Deprecated
- `service.CompactTxStreamer.GetTaddressTxids`. Use `GetTaddressTransactions`
  instead.

## [v0.3.5] - 2023-07-03

### Added
- `compact_formats.ChainMetadata`
- `service.ShieldedProtocol`
- `service.GetSubtreeRootsArg`
- `service.SubtreeRoot`
- `service.CompactTxStreamer.GetBlockNullifiers`
- `service.CompactTxStreamer.GetBlockRangeNullifiers`
- `service.CompactTxStreamer.SubtreeRoots`

### Changed
- `compact_formats.CompactBlock` has added field `chainMetadata`
- `compact_formats.CompactSaplingOutput.epk` has been renamed to `ephemeralKey`

## [v0.3.4] - UNKNOWN

### Added
- `service.CompactTxStreamer.GetLatestTreeState`

## [v0.3.3] - 2022-04-02

### Added
- `service.TreeState` has added field `orchardTree`

### Changed
- `service.TreeState.tree` has been renamed to `saplingTree`

## [v0.3.2] - 2021-12-09

### Changed
- `compact_formats.CompactOrchardAction.encCiphertext` has been renamed to
  `CompactOrchardAction.ciphertext`

## [v0.3.1] - 2021-12-09

### Added
- `compact_formats.CompactOrchardAction`
- `service.CompactTxStreamer.GetMempoolTx` (removed in 0.3.0) has been reintroduced.
- `service.Exclude` (removed in 0.3.0) has been reintroduced.

### Changed
- `compact_formats.CompactSpend` has been renamed `CompactSaplingSpend`
- `compact_formats.CompactOutput` has been renamed `CompactSaplingOutput`

## [v0.3.0] - 2021-07-23

### Added
- `service.CompactTxStreamer.GetMempoolStream`

### Removed
- `service.CompactTxStreamer.GetMempoolTx` has been replaced by `GetMempoolStream`
- `service.Exclude` has been removed as it is now unused.

## [v0.2.4] - 2021-01-14

### Changed
- `service.GetAddressUtxosArg.address` has been replaced by the
  repeated field `addresses`. This is a [conditionally-safe](https://protobuf.dev/programming-guides/proto3/#conditionally-safe-changes)
  format change.
- `service.GetAddressUtxosReply` has added field `address`

## [v0.2.3] - 2021-01-14

### Added
- `service.LightdInfo` has added fields:
  - `estimatedHeight`
  - `zcashdBuild`
  - `zcashdSubversion`

## [v0.2.2] - 2020-10-22

### Added
- `service.TreeState`
- `service.GetAddressUtxosArg`
- `service.GetAddressUtxosReply`
- `service.GetAddressUtxosReplyList`
- `service.CompactTxStreamer.GetTreeState`
- `service.CompactTxStreamer.GetAddressUtxos`
- `service.CompactTxStreamer.GetAddressUtxosStream`

## [v0.2.1] - 2020-10-06

### Added
- `service.Address`
- `service.AddressList`
- `service.Balance`
- `service.Exclude`
- `service.CompactTxStreamer.GetTaddressBalance`
- `service.CompactTxStreamer.GetTaddressBalanceStream`
- `service.CompactTxStreamer.GetMempoolTx`
- `service.LightdInfo` has added fields:
  - `gitCommit`
  - `branch`
  - `buildDate`
  - `buildUser`

## [v0.2.0] - 2020-04-24

### Added
- `service.Duration`
- `service.PingResponse`
- `service.CompactTxStreamer.Ping`

### Removed
- `service.TransparentAddress` was removed (it was unused in any service API).

## [v0.1.1] - 2019-11-27

### Added
- `service.Empty`
- `service.LightdInfo`
- `service.TransparentAddress`
- `service.TransparentAddressBlockFilter`
- `service.CompactTxStreamer.GetTaddressTxids`
- `service.CompactTxStreamer.GetLightdInfo`
- `service.RawTransaction` has added field `height`

## [v0.1.0] - 2019-09-19

Initial release
