# bufplugin

[![Build](https://github.com/bufbuild/bufplugin/actions/workflows/ci.yaml/badge.svg?branch=main)](https://github.com/bufbuild/bufplugin/actions/workflows/ci.yaml)
[![BSR](https://img.shields.io/badge/BSR-Module-0C65EC)](https://buf.build/bufbuild/bufplugin)
![License](https://img.shields.io/github/license/bufbuild/bufplugin)
[![Slack](https://img.shields.io/badge/Slack-Buf-%23e01563)](https://buf.build/links/slack)

Bufplugin is Buf's framework for authoring plugins that work with the Buf CLI and Buf Schema
Registry. Currently, this provides an API for custom lint and breaking change plugins, so users can
implement their own lint and breaking change rules.

This repository contains the Protobuf APIs that comprise the bufplugin framework. Buf plugins are
implemented using [PluginRPC](https://github.com/pluginrpc/pluginrpc). The entrypoint for custom
lint and breaking change plugins is the [CheckService](buf/plugin/check/v1/check_service.proto). A
plugin is simply an implementation of the `CheckService` served via `PluginRPC` in a built binary.

While the APIs provide a mechanism to implement a Buf plugin in any language, we provide
[bufplugin-go](https://github.com/bufbuild/bufplugin-go) as an easy way to author Buf plugins in Go.
We would highly recommend starting there: **bufplugin-go is the best way to author custom lint and
breaking change plugins, and is likely the repository you are looking for.**

See [buf.build/bufbuild/bufplugin](https://buf.build/bufbuild/bufplugin) for all API documentation.

## Status: Beta

Bufplugin is currently in beta, and may change as we work with early adopters. We're intending to
ship a stable v1.0 by the end of 2024. However, we believe the API is near its final shape.

## Legal

Offered under the [Apache 2 license](https://github.com/bufbuild/bufplugin/blob/main/LICENSE)
