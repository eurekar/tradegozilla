# Trade Go-zilla

A Go-based API client for the [TradeMonster](https://www.trademonster.com) API.

## Getting Started

### Installation

Add the appropriate import entry to you project:

```go
import (
    "github.com/glenngillen/tradegozilla"
)
```

And then run `go get`.

### Usage

Here's a simple example to retrieve the quote information for "AAPL":

```go
func main() {
    client, _ := tradegozilla.MonsterClient{}.NewClient()
    client.Auth()
    quote, _ := client.Quote([]string{"AAPL"})
    fmt.Printf("Quote is: %s\n", quote)
}
```

Right now there is **zero error-handling** :(. This is very much still a work in progress.

## Further Reading

The official TradeMonster API documentation is appalling and every API call I've looked at so for
is either documented incorrectly or incompletley. The officially recommended way to work out how to
use the API is to use [Charles](http://www.charlesproxy.com) as a proxy server to [Man-in-the-middle](http://en.wikipedia.org/wiki/Man-in-the-middle_attack)
yourself and reverse-engineer their entire trading platform yourself. Astounding for an API that requires
you to deposit $30K to get access to it.

As a result I've been trying to document generate [complete API documentation](http://trademonster.glenngillen.com) as I go, but
can make no guarantees to it's accuracy or completeness as TradeMonster could change anything at any time without
informing me.

## Compatibility

## Status

In active development and heavy refactoring, it's unstable and shouldn't be relied upon in production.

## Contributing

Patches and pull requests are gladly accepted. Please make sure that you include associated tests and documentation and that your commit messages are brief but descriptive.

## Credits & Contributions

## License

Tradegozilla is released under the MIT license.

Copyright (c) 2015 Glenn Gillen

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

[![Analytics](https://ga-beacon.appspot.com/UA-46840117-1/tradegozilla/readme?pixel)](https://github.com/igrigorik/ga-beacon)
