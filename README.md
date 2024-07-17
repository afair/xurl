# xurl

Wrapper script to curl with curated options and meta options

Usage: xurl [method] URL [name=value] [+xurl options] [-curl options]

* method: GET POST PUT DELETE PATCH
* name=value           -- Param pairs, use curl features like @filename
* +xurloption[=value]  -- xurl meta-options
  * +auth=userC[:pass] -- API keys, HTTP Basic Auth
  * +j[son]            -- Ask for JSON response
  * +y[aml]            -- Ask for YAML response
  * +save|+o           -- Save with name in URL, like wget
  * +p[roxy] [user:pw@]host:port -- HTTP Proxy server
  * +d[ebug]           -- Prints command, issues curl info
* -curlopt --curl-option -- Option to pass to curl

* Env: XURL_ARGS="..." to add default curl options.
* Follow redirect is enabled, BUT it will not forward data in POST requests.
