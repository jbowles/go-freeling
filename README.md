# go-freeling

http://localhost:9999/analyzer?url=https://www.reservationcounter.com/hotels/show/124363/caesars-palace/?check-in=&check-out=&random=864127

http://localhost:9999/analyzer?url=https://www.expedia.com/Las-Vegas-Hotels-Caesars-Palace.h41245.Hotel-Information?rm1=a2&hwrqCacheKey=c85d363c-f662-4015-a56e-60c533e0c4f6HWRQ1458248342526&c=73e02088-fd27-45d2-b627-046d13551d17&&chkin=03%2F24%2F2016&chkout=03%2F25%2F2016

**Natural Language Processing** in GO

This is a partial port of Freeling 3.1 (http://nlp.lsi.upc.edu/freeling/).

License is GPL to respect the License model of Freeling.

This is the list of features already implemented:

* Text tokenization
* Sentence splitting
* Morphological analysis
* Suffix treatment, retokenization of clitic pronouns
* Flexible multiword recognition
* Contraction splitting
* Probabilistic prediction of unknown word categories
* Named entity detection
* PoS tagging
* Chart-based shallow parsing
* Named entity classification (With an external library MITIE - https://github.com/mit-nlp/MITIE)
* Rule-based dependency parsing

-

**How to use it**:

go build gofreeling.go

./gofreeling

(http server listens on default port 9999 - port can be changed in conf/gofreeling.toml file)

To process a page:

HTTP GET: *http://localhost:9999/analyzer?url=COPY HERE AN URL*

Response is a self-explaining json

-
TODO:
* clean code
* add comments
* add tests
* implement WordNet-based sense annotation and disambiguation

-
**Linguistic Data** to run the server can be download here (English only):

https://www.dropbox.com/s/fwwvfxp2s7dydet/data.zip
