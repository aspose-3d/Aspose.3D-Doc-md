---
title: Macos'ta libgdiplus nasıl kurulur
type: docs
description: Bu makale, monterey 12.4 gibi macos'ta libgdiplus'ın nasıl kurulacağını açıklıyor
weight: 150
url: /tr/net/how-to-install-libgdiplus-in-macos/
---
## Macos'ta homebrew yükleyin

Aşağıdaki komutu terminalde çalıştırarak macos'ta pfl'yi yükleyebilirsiniz.

```cs

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

```

## Macos'ta libgdiplus yükleyin

Bret'yi kurduktan sonra, libgdiplus'ı macos'a yükleyebilirsiniz:

```cs

brew install mono-libgdiplus

```
