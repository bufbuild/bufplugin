# bufplugin

[![Build](https://github.com/bufbuild/bufplugin/actions/workflows/ci.yaml/badge.svg?branch=main)](https://github.com/bufbuild/bufplugin/actions/workflows/ci.yaml)
[![BSR](https://img.shields.io/badge/BSR-Module-0C65EC)](https://buf.build/bufbuild/bufplugin)
![License](https://img.shields.io/github/license/bufbuild/bufplugin)
[![Slack](https://img.shields.io/badge/Slack-Buf-%23e01563)](https://buf.build/links/slack)

Bufplugin is Buf's framework for authoring plugins that work with the Buf CLI and Buf Schema
Registry. We're starting out by providing a way to implement custom lint and breaking change
plugins, so users can implement their own lint and breaking change rules.

This repository contains the Protobuf APIs that comprise the bufplugin framework. Buf plugins are
implemented using the [PluginRPC](https://github.com/pluginrpc/pluginrpc) RPC framework.

While you can implement a Buf plugin in any language, we provide
[bufplugin-go](https://github.com/bufbuild/bufplugin-go) as an easy way to author Buf plugins in Go.
We'd highly recommend starting there.

## Status: Alpha

Bufplugin is as early as it gets - [buf](https://github.com/bufbuild/buf) doesn't actually support
plugins yet! We're publishing this publicly to get early feedback as we approach stability.

## Legal

Offered under the [Apache 2 license](https://github.com/bufbuild/bufplugin/blob/main/LICENSE)
