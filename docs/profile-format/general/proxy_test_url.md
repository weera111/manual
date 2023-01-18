---
sidebar_position: 3
---

# `proxy-test-url`

Test url used by [url-test](/docs/profile-format/proxygroup/auto) and manually node speed test.

Non-direct proxy will use this url. For [direct proxy](/docs/profile-format/proxy/built-in-proxy/direct), please refer to [`internet-test-url`](./internet_test_url)

An `HTTP HEAD` request will be sent towards this url

An `HTTP/1.1 204 No Content` response is expected.

## Sample

```ini
proxy-test-url = http://www.gstatic.com/generate_204
```

## Format

```ini
proxy-test-url = {http_url}
```

:::tip
`url` should start with `http://`, `https://` or other scheme uri is not supported
:::

:::tip
You can emulate proxy test by using command below:
```shell
curl -I http://www.gstatic.com/generate_204
```
:::
