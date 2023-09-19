
Not only shortens URLs but also counts and give you access to the metrics and other features like shields.io badge!

--- 

### Creating a shortURL


    POST https://visitly.paodayag.dev/create

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

### Displaying number of visits as shields.io badge

Badge Image URL:

    https://visitly.paodayag.dev/{name}/badge

Example Markdown:

    ![Number of installs](https://visitly.paodayag.dev/linuxserver.zip/badge?label=Installs)

Example HTML:

    <img src="https://visitly.paodayag.dev/linuxserver.zip/badge?label=Installs" alt="Number of installs" />

Example Display:

![Number of installs](https://visitly.paodayag.dev/linuxserver.zip/badge?label=Installs)


#### Customization Options

| Option | Description |
| --- | --- |
| label | Custom badge label. Default: `Visits` |
| labelColor | Background color for the label. Default: `#555` |
| color | Background color for the visits count. Default `#4c1` |

---

### Getting the visits count information

URL:

    https://visitly.paodayag.dev/{name}/info

Example Response:

    {
    	"_id": "linuxserver.zip",
    	"url": "https://github.com/WisdomSky/CasaOS-LinuxServer-AppStore/archive/refs/heads/main.zip",
    	"visits": 1825083,
    	"last_updated": "09-19-2023 09:29:50PM UTC"
    }

---

### Viewing the detailed visits count history (Not yet available)

    https://visitly.paodayag.dev/{name}/history


