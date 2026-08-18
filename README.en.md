<div align="center">
  <img src="./app/src/main/ic_launcher-round.png" alt="Phoenix" width="128" height="128">
  <h1>Phoenix</h1>

[![GitHub release](https://img.shields.io/github/v/release/h3110w0r1d-y/Phoenix)](https://github.com/h3110w0r1d-y/Phoenix/releases)
[![CI/CD](https://github.com/h3110w0r1d-y/Phoenix/actions/workflows/release.yml/badge.svg)](https://github.com/h3110w0r1d-y/Phoenix/actions/workflows/release.yml)
![Android](https://img.shields.io/badge/Android-8.0%2B-blue)
![License](https://img.shields.io/github/license/h3110w0r1d-y/Phoenix)
![GitHub stars](https://img.shields.io/github/stars/h3110w0r1d-y/Phoenix?style=social)
</div>

---

[简体中文](README.md) | English

## About

Based on Xposed. It hooks the process creation functions of the system framework and
changes the MaxOomAdj of a process to keep app processes alive.

Android 8+ is supported in theory. Hook location:
[Hook.kt](./app/src/main/java/com/h3110w0r1d/phoenix/hook/Hook.kt). It has only been
tested on Android 15~16, so use it with caution on other versions.

## Download

  - [Latest Release](https://github.com/h3110w0r1d-y/Phoenix/releases/latest)

## Usage

  - Open LSPosed, enable the module, select `System Framework` only, and reboot the
    system for the module to take effect
  - Open the module and check the apps you want to keep alive (Android 10+ takes effect
    immediately, without restarting the system or the app; below Android 10 the app has
    to be restarted)

## Screenshots

<details>
    <summary>Click to expand the screenshots</summary>
    <img src="img/home.png" width="300">
    <img src="img/app.png" width="300">
    <img src="img/setting.png" width="300">
</details>

## Language

The app follows the system language. A device in Chinese shows the original Simplified
Chinese text; every other language falls back to English, which is the default resource
set.

To choose the language explicitly, use the per-app language preference of Android 13+:
**Settings › Apps › Phoenix › Language**.

## Roadmap

  - [x] Configure the default MaxAdj
  - [x] Configure a different MaxAdj per app
  - [x] Support for enabling Persistent
  - [x] Activity keep-alive (Android 11+)
  - [x] Service keep-alive (TargetApi < 34)

Suggestions and problems are welcome: open an Issue, or join the QQ group 1083682874.

## Donate

<img src="img/wechat.png" width="300">
<img src="img/alipay.jpg" width="300">

## ❤️Sponsors

- [Jie0746](https://github.com/Jie0746)
