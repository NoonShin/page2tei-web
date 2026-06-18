# page2tei-web

A browser-based converter from PAGE XML to TEI, built on top of 
[page2tei](https://github.com/dariok/page2tei) by Dario Kampkaspar.

## Quick factsheet

- Static web application with no installation required and no data collection
- Processes PAGE XML files directly (no METS required)
- Metadata entry via form or by uploading a METS file
- Outputs one TEI file per page
- Handles both Transkribus (2013 namespace) and eScriptorium (2019 namespace) exports

## Use it

→ [noonshin.github.io/page2tei-web](https://noonshin.github.io/page2tei-web)

## Development

The modified XSLT (`page2tei-web.xsl`) is compiled to `docs/page2tei.sef.json` using
[Saxon-JS](https://www.saxonica.com/saxon-js/index.xml):

    xslt3 -xsl:page2tei-web.xsl -export:docs/page2tei.sef.json -nogo -relocate:on

## Credits

XSLT logic by [Dario Kampkaspar](https://github.com/dariok/page2tei), 
licensed under MIT. This fork modifies the stylesheet for browser execution 
and adds the web interface.
