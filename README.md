# https://vistr.dev - A visitor counter for your GitHub projects

![](https://vistr.dev/badge?repo=Elfocrash.visitr.dev)

## Usage

Simply add `![](https://vistr.dev/badge?repo=yourUsername.repoName)` inside your README.md file and voila, you are not countring all the visitors to your project.

Please note that it will **ONLY** work on GitHub. If you try to access the link from your browser you will get an error.

## Customisation

There are a few customisations that you can apply. If you want me to add more please create an issue of a PR to submit your suggestions.

| Query param name | Possible values                      | Example value      | Description                                         |
|------------------|--------------------------------------|--------------------|-----------------------------------------------------|
| color            | Any hex color value without the hash | color=0000FF       | Changes the color of the "number" part of the badge |
| leftcolor        | Any hex color value without the hash | color=0000FF       | Changes the color of the "text" part of the badge   |
| text             | Any text                             | Project%20visitors | Overrides the default "visitors" text               |
| corners          | round/square                         | round              | Overrides the default rounded corners on the badge  |

## Disclaimer

There is **absolutely nothing** being tracked except for the visitor count. In fact, I am unable to create graphs out of this data because I don't store them in an entry by entry fashion but instead I am just incrementing a counter atomically. Also because the requests are coming via GitHub's camo (CDN) service and not through your browser, I can't really see any information even if I wanted to.

I didn't want to host this on a free hosting service because you would get throttling errors, cold starts and all that non-sense. For that reason I chose to pay for the hosting. Don't worry it runs on Azure Functions and Cosmos DB so it's scaleable and blazing fast but it does mean that I have to pay a small amount of money each month. 
There is no way I would ever charge for something as simple as this but if you want to support me then please consider becoming a [GitHub sponsor](https://github.com/sponsors/Elfocrash).
