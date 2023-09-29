
Visit.ly not only shortens URLs but also counts and lets you display metrics as badge and charts!

--- 

# Create

> &nbsp;**POST**&nbsp;&nbsp;&nbsp;&nbsp;`https://visitly.paodayag.dev/create`

Body:

    {
        "name": "my-website",
        "url": "https://my-awesome.website/"
    }

Example Response:

    {
        "success": true,
        "message": "Created successfully. Your Visitly short URL is https://visitly.paodayag.dev/my-website"
    }

---

# Retrieving Info

URL:

> &nbsp;**GET**&nbsp;&nbsp;&nbsp;&nbsp;`https://visitly.paodayag.dev/{name}/info`

    
Example Response:

    {
    	"name": "linuxserver.zip",
    	"url": "https://github.com/WisdomSky/CasaOS-LinuxServer-AppStore/archive/refs/heads/main.zip",
    	"visits": 1825083,
        "visits_unique": 12345,
    	"last_updated": "09-19-2023 09:29:50PM UTC"
    }

---


# Badges

> &nbsp;**GET**&nbsp;&nbsp;&nbsp;&nbsp;`https://visitly.paodayag.dev/{name}/badge`


#### Options

| Option | Description |
| --- | --- |
| unique | Shows unique visitors. Default: `false` |
| label | Custom badge label. Default: `Visits` |
| labelColor | Background color for the label. Default: `#555` |
| color | Background color for the visits count. Default `#4c1` |

#### Total Visits Badge

> &nbsp;**GET**&nbsp;&nbsp;&nbsp;&nbsp;`https://visitly.paodayag.dev/{name}/badge?label=Unique%20Visits`

Example:

![Total Visits](https://visitly.paodayag.dev/linuxserver.zip/badge?label=Total%20Visits)

#### Unique Visits Badge

> &nbsp;**GET**&nbsp;&nbsp;&nbsp;&nbsp;`https://visitly.paodayag.dev/{name}/badge?unique=1&label=Unique%20Visits`

Example:

![Unique Visits](https://visitly.paodayag.dev/linuxserver.zip/badge?unique=1&label=Unique%20Visits)


### Displaying Badges

Markdown:

```markdown
![Number of installs](https://visitly.paodayag.dev/linuxserver.zip/badge?label=Installs)
```

HTML:

```html
<img src="https://visitly.paodayag.dev/linuxserver.zip/badge?label=Installs" alt="Number of installs" />
```
---

# Charts

> &nbsp;**GET**&nbsp;&nbsp;&nbsp;&nbsp;`https://visitly.paodayag.dev/{name}/chart`

#### Options

| Option | Description |
| --- | --- |
| type | Type of chart . Default: `daily` |
| unique | Shows unique visitors. Default: `false` |

See [Chart.js](https://www.chartjs.org/docs/latest/configuration/#options) for other applicable options.


#### Daily Visits Chart

> &nbsp;**GET**&nbsp;&nbsp;&nbsp;&nbsp;`https://visitly.paodayag.dev/{name}/chart`

Example:

![Total Visits](https://visitly.paodayag.dev/linuxserver.zip/chart)

#### Unique Daily Visits Badge

> &nbsp;**GET**&nbsp;&nbsp;&nbsp;&nbsp;`https://visitly.paodayag.dev/{name}/chart?unique=1`

Example:

![Unique Visits](https://visitly.paodayag.dev/linuxserver.zip/chart?unique=1)


#### Monthly Visits Chart

> &nbsp;**GET**&nbsp;&nbsp;&nbsp;&nbsp;`https://visitly.paodayag.dev/{name}/chart?type=monthly`

Example:

![Total Visits](https://visitly.paodayag.dev/linuxserver.zip/chart?type=monthly)

#### Unique Monthly Visits Badge

> &nbsp;**GET**&nbsp;&nbsp;&nbsp;&nbsp;`https://visitly.paodayag.dev/{name}/chart?unique=1&type=monthly`

Example:

![Unique Visits](https://visitly.paodayag.dev/linuxserver.zip/chart?unique=1&type=monthly)


### Displaying Charts

Markdown:

```markdown
![Chart](https://visitly.paodayag.dev/linuxserver.zip/chart)
```

HTML:

```html
<img src="https://visitly.paodayag.dev/linuxserver.zip/chart" alt="Chart" />
```


