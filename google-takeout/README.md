# Google Takeout

1. Install the extension [Get cookies.txt LOCALLY](https://chromewebstore.google.com/detail/get-cookiestxt-locally/cclelndahbckbenkjhflpdbgdldlbecc) and copy the cookies for your Google session on Google takeout.
2. Paste them in `cookies.txt`
3. Download with wget cookies and redirection

```bash
wget -c --load-cookies cookies.txt <GOOGLE_TAKEOUT_LINK>
```

4. Import zip file to immich with [immich-go](https://github.com/simulot/immich-go)

```bash
immich-go upload from-google-photos --server=http://localhost:2283 --api-key=$IMMICH_API_KEY /path/to/takeout-*.zip
```
