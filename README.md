# ☁️ get-cloudflare-location
A JavaScript function to get user's location based on Cloudflare `/cdn-cgi/trace`

## How it works

This function will send a request to `https://www.cloudflare.com/cdn-cgi/trace` and `https://cf-ns.com/cdn-cgi/trace` and parse the response to get the user's location.

## Usage

``` bash
npm install get-cloudflare-location
```

``` ts
import getCloudflareLocation from "get-cloudflare-location";

interface GetCloudflareLocationOptions {
  timeout?: number; // The timeout for the request in milliseconds. Defaults to 5000
  cache?: string; // Whether to cache the result of the request. Defaults to true.
}

const options: GetCloudflareLocationOptions | undefined = {
  timeout: 5000,
  cache: true,
};

const location = await getCloudflareLocation(options);
```


## License

MIT
