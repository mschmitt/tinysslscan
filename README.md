As it says on the label, this is a pure bash + openssl SSL cipher scanner for
cases where nothing™ can be installed. 

This wraps the openssl s_client command and thus should also accept the -key
and -cert options, although I haven't had the opportunity to test them yet.

```
tinysslscan host:port [-starttls smtp]
            ^^^^^^^^^^^^^^^^^^^^^^^^^^ As with openssl s_client
```

### Alternatives

The easiest to use alternative, even preinstalled on many systems, is probably
nmap (the script even claims it does automatic STARTTLS where required):

```
nmap -sV --script ssl-enum-ciphers -p port host
```

### Disclaimer

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.

[modeline]: # ( vim: set fenc=utf-8 textwidth=78 formatoptions=tan: )
