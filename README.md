# pacwget
Get web URLs, robustly trying multiple proxies and servers, supporting Proxy Auto Config

pacwget is a wrapper to [GNU wget](http://www.gnu.org/software/wget/) that will try all available web proxies
and servers if any of them fail.  Proxies come from $http_proxy which can be a round-robin DNS name, from
$HTTP_PROXIES which is a list of proxies, or from
[Web Proxy Auto Discovery](http://en.wikipedia.org/wiki/Web_Proxy_Autodiscovery_Protocol) URLs (which are
[Proxy Auto Config](http://en.wikipedia.org/wiki/Proxy_auto-config) format) found in $PAC_URLS.  Servers come from
round-robin names in the target URL.  Also has an --only-proxies option which just prints the list of proxies
parsed from the PAC file instead of downloading given URL.  Requires [pacparser](https://github.com/pacparser/pacparser)
library and wget.

The files in this package are planned to be merged into the pacparser library at some point.
