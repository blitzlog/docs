## Getting Started

Use `github.com/blitzlog/log` package in your `GoLang` source code for publishing logs. By default this prints logs to `stdout`, to stream logs to *BlitzLog* platform, follow the steps below.

## Register at [blitzlog.com](https://test.blitzlog.com)

- Login using your Google account.
- Create a new account if not already created.
- Go to `Settings` tab, followed by `Keys` sub-tab.
- Create API Key, or use existing one.

## Use API key in go source

Update your code entrypoint to look something like below.

```
import (
	...
	"github.com/blitzlog/log"
)

func main() {
	defer log.Flush()                           // flush all logs before returning
	log.SetAPIKey("APIKEYOBTAINEDFROMBLITZLOG") // api key for authenticating /w remote server
	doMain()                                    // run main method
}

```

Thats is all, run your code a local machine, on-prem or public cloud, which allows outbound TCP traffic.

You can view your logs at [blitzlog.com](https://test.blitzlog.com).
