# semi-static-proxy-ips
Lists of semi-static open proxy exit IPs, updated weekly

## Introduction

As a complement to my February 2024 research study titled <a href="https://mannfred.com/open-proxy-life-expectancy/">Open Proxy Life Expectancy</a> a set of CSV files containing semi-static open proxy exit IPs are provided.

## Datasets

The following semi-static exit IP datasets are available:

| List | Description |
| --- | --- |
| ![proxy_exits_7d_ipv4.csv](https://github.com/mannfredcom/semi-static-proxy-ips/blob/main/proxy_exits_7d_ipv4.csv) | List of open proxy exit IPv4 IPs which have been active for 7 days or longer |
| ![proxy_exits_7d_ipv6.csv](https://github.com/mannfredcom/semi-static-proxy-ips/blob/main/proxy_exits_7d_ipv6.csv) | List of open proxy exit IPv6 IPs which have been active for 7 days or longer |
| ![proxy_exits_30d_ipv4.csv](https://github.com/mannfredcom/semi-static-proxy-ips/blob/main/proxy_exits_30d_ipv4.csv) | List of open proxy exit IPv4 IPs which have been active for 30 days or longer |
| ![proxy_exits_30d_ipv6.csv](https://github.com/mannfredcom/semi-static-proxy-ips/blob/main/proxy_exits_30d_ipv6.csv) | List of open proxy exit IPv6 IPs which have been active for 30 days or longer |

In cases where the exit IP(s) differ(s) from the entry IP the entry information is included in the comment field. Entry ports and protocols are omitted from the data to reduce the risk of abuse.

Additionally, lists of proxy exit subnets with more activity than usual (16 or more unique IP detections per subnet) are extracted from the semi-static exit data for convenience:

| List | Description |
| --- | --- |
| ![proxy_subnets_7d_ipv4.csv](https://github.com/mannfredcom/semi-static-proxy-ips/blob/main/proxy_subnets_7d_ipv4.csv) | High activity IPv4 proxy subnets which have been active for 7 days or longer |
| ![proxy_subnets_7d_ipv6.csv](https://github.com/mannfredcom/semi-static-proxy-ips/blob/main/proxy_subnets_7d_ipv6.csv) | High activity IPv6 proxy subnets which have been active for 7 days or longer |
| ![proxy_subnets_30d_ipv4.csv](https://github.com/mannfredcom/semi-static-proxy-ips/blob/main/proxy_subnets_30d_ipv4.csv) | High activity IPv4 proxy subnets which have been active for 30 days or longer |
| ![proxy_subnets_30d_ipv6.csv](https://github.com/mannfredcom/semi-static-proxy-ips/blob/main/proxy_subnets_30d_ipv6.csv) | High activity IPv6 proxy subnets which have been active for 30 days or longer |

Notes:
- The IPv4 subnet search is simplistic and simply matches exit IPs against /24 subnets.
- For the IPv6 search a dynamic prefix length (with a /4 boundary) is used. As the potential IP space is generally massive the search is limited to exit IPs associated with specific entry IPs. Thus, whatever prefix length may have been fitted to the data, a single entry point had access to the entire range.
