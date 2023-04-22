# toolsExplainedz

## Alternatives

Installing a new version of Golang.

This method allows multiple versions of Golang to coexist.

Downloading the new compiler

```bash
$ sha256sum /home/panhong/下載/go1.20.3.linux-amd64.tar.gz
# 979694c2c25c735755bf26f4f45e19e64e4811d661dd07b8c010f7a8e18adfca
# (Copy and paste the SHA256 checksum and search for it on the website.)
```

Perform alternative installation

```bash
# Place the new version of the golang folder
$ sudo cp /home/panhong/下載/go1.20.3.linux-amd64.tar.gz /usr/local/
$ sudo su -
$ cd /usr/local/
$ tar -zxvf go1.20.3.linux-amd64.tar.gz -C ./
$ mv go go-1.20.3

# Set up the new version of golang
$ update-alternatives --install /usr/bin/go go /usr/local/go-1.20.3/bin/go 150 --slave /usr/bin/gofmt gofmt /usr/local/go-1.20.3/bin/gofmt
$ update-alternatives --config go

# Remove the old version of golang
$ update-alternatives --remove go /usr/local/go-1.19.2/bin/go

# Run the new version of golang
$ exit # Exit root
$ go version
# go version go1.20.1 linux/amd64
```

Use the following command to remove the old version of Golang:

```bash
$ update-alternatives --list go
# /usr/lib/go-1.15/bin/go
# /usr/local/go-1.19.2/bin/go # remove !
# /usr/local/go-1.20.1/bin/go
# /usr/local/go-1.9/bin/go

$ sudo rm /usr/local/go1.19.2.linux-amd64.tar.gz
$ sudo update-alternatives --remove go /usr/local/go-1.19.2/bin/go
$ sudo rm -rf /usr/local/go-1.19.2
```

## Goland

### External tools settings

> [Jetbrains Reference](https://www.jetbrains.com/help/idea/settings-tools-external-tools.html)

typora

| options           | parameters               |
| ----------------- | ------------------------ |
| name              | typora                   |
| program           | /usr/bin/typora          |
| arguments         | $ContentRoot$/$FileName$ |
| working directory | $ProjectFileDir$         |

<img src="/home/panhong/go/src/github.com/panhongrainbow/toolsExplainedz/assets/image-20230422111907930.png" alt="image-20230422111907930" style="zoom:80%;" /> 

## AI tools

### Claude

[Slack Login](https://slack.com/intl/zh-tw/)

[Add To Slack](https://www.anthropic.com/claude-in-slack)

### ChatGPT

[ChatGPT Desktop In Sanp](https://snapcraft.io/chatgpt-desktop)

### Perplexity

[Perplexity In Web](https://www.perplexity.ai/)

[Perplexity In Edge](https://chrome.google.com/webstore/detail/perplexity-ask-ai/hlgbcneanomplepojfcnclggenpcoldo/related)















