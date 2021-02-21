# lv-dropbox

lv-dropbox is a partial implementation of the (Dropbox v2 API)[https://www.dropbox.com/developers/documentation/http/documentation]. It implements OAUTH2 authentication (although the token method makes the most sense for expected applications) and methods for download, upload, listing folders and creating/sharing links for files.

## Known Issues

The challenge authentication for SHA256 is janky/non-functional at the moment. Not 100% sure why.

## OAuth2

See the following links for more information:

* https://www.dropbox.com/lp/developers/reference/oauth-guide
* https://oauth.net/

LabVIEW doesn't have support for URL fragmenets, so legacy implementation of OAuth1 is inherently unsupported. As a result, OAuth2 will allow authentication using a variety of **secure** methods. For situations where you need to authenticate client-side, having a built-in webserver listening on the localhost seems to be the best implementation.

See (example_01_authorization.vi)[./source/lv-dropbox/examples/public/example_01_authorization.vi] to see implementations of OAuth2.

## v2 API

### Examples:

