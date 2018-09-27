# Getting Started

Use `github.com/blitzlog/log` package in your `GoLang` source code for publishing logs. By default this prints logs
to `stdout`. To stream logs to *BlitzLog* platform, follow the 2 step process below.

## Register at `blitzlog.com`

- Use your Google account to login at https://blitzlog.com.
- Create a new account if you have not already create one.
- Click on `Settings` tab, followed by `Keys` sub-tab.
- Use an existing API Key, or create a new one.

## Update go source to use API Key

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

Thats is all, run your code locally or in any public cloud env like Digital Oceam, AWS, GCP, or, Azure.

You can view your logs at https://blitzlog.com using the same login, used to create API Key.
