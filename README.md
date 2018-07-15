Cloudflare Challenge Solver
===========================

A port of [cloudflare-scrape](https://github.com/Anorov/cloudflare-scrape).

Usage
-----

```go
package main

import (
    "github.com/abc1236762/go-cloudflare-scraper"
)

func main() {
	var err error
	
	var client = scraper.NewClient()
	if res, err = client.Get("<URL here>"); err != nil {
		log.Fatal(err)
	}
	
	var body []byte
	if body, err = ioutil.ReadAll(res.Body); err != nil {
		log.Fatal(err)
	}
	defer res.Body.Close()
	
}
```
