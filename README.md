# Country with states and dial code

List of countries with states on country code param, ready to serve as static content.


## Usage

This can be used right away with get request to [https://countries.bloggernepal.com/countries/](https://countries.bloggernepal.com/countries/). It can be used for testing or smaller project, but as this is served from github it can get limited requests, so just clone on your server and serve these files as static files.

Git repo: [https://github.com/InfoDevkota/Country-with-states-and-dial-code](https://github.com/InfoDevkota/Country-with-states-and-dial-code)

Let's assume it is cloned and served through `/static`.

`/static/countries/` or to `/static/countries.json` will return all the countries with country code, name, capital, region [32.5 kb]

```
[{
    "code": "NP",
    "code3": "NPL",
    "name": "Nepal",
    "capital": "Kathmandu",
    "region": "Asia",
    "subregion": "Southern Asia",
    "dialCode": "+977"
}, ..., {}]
```

 `/static/countries-mini/` or `/static/countries-mini.json`  will return mini version [8.5kb]
```
[{
    "code": "NP",
    "name": "Nepal"
}, ..., {}]
```

Once we got the `code` for country, we can request for it's states and other details with `/static/states/NP/` or `/static/states/NP.json`, NP being the country code.

```
{
    "code": "NP",
    "code3": "NPL",
    "name": "Nepal",
    "capital": "Kathmandu",
    "region": "Asia",
    "subregion": "Southern Asia",
    "states": [
        {
            "code": "4",
            "name": "Gandaki"
        }, ..., {}
    ],
    "dialCode": "+977"
}
```

## Data Used
[https://github.com/stefanbinder/countries-states](https://github.com/stefanbinder/countries-states)

[https://gist.github.com/Goles/3196253](https://gist.github.com/Goles/3196253)


## Contributing
These data are not complete or can be outdated. Pull requests are welcome.

## License
MIT
