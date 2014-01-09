Project Hub + Harp
==================

__A Harp Boilerplate for Brad Frost’s [Project Hub](https://github.com/bradfrost/project-hub) HTML template__

Read more about [project hubs on 24 Ways.](http://24ways.org/2013/project-hubs/)

This is an HTML template for online project timelines (also known as "project hubs").

## What is a project hub and why would I use one?

A project hub is a tool for keeping track of the progress of a design project. The hub lives online (either publically available or password protected), so that everyone involved in the team has access to it.

The benefits of using a project hub:
- Serves as a centralized place for the project's key design/development materials
- Easily and visually view project progress
- Provides an archive for project artifacts
- Keep clients and team members up to speed with design progress
- Lives at a URL that doesn't change

## Resources

- [Original HTML Template](https://github.com/bradfrost/project-hub)
- [Overview of project hubs on 24 Ways.](http://24ways.org/2013/project-hubs/)
- [Getting Started with Harp](http://harpjs.com/docs/quick-start)

## Getting started

1) Install Harp in your computer

```
$ sudo npm install -g harp
```

2) Clone this repository
```
$ git clone git@github.com:jorgepedret/harp-project-hub.git
```

3) Start Harp server
```
$ harp server harp-project-hub
```

4) Visit [http://localhost:9000/](http://localhost:9000/) in your browser and follow the instructions in the page

## How to add new events to the timeline

After you rename `_data-sample.json` to `_data.json`, the data structure is fairly simple to understand.

1. Open your `_data.json` file
2. Add a new item to the `timeline` container

```
{
  "timeline": [
    {
      "stamp": "August 9th, 2013",
      "content": "Sign contract",
      "links": {
        "View contract": "#"
      }
    }
  ]
}
```

If you wanna add a new one, simply append it to the top, like this:

```
{
  "timeline": [
    {
      "stamp": "August 14th, 2013",
      "content": "Kickoff Meeting",
      "links": {
        "View notes": "#",
        "View demo": "#"
      }
    },
    {
      "stamp": "August 9th, 2013",
      "content": "Sign contract",
      "links": {
        "View contract": "#"
      }
    }
  ]
}
```

> Tip: Comas and quotes are important when writing JSON. Follow the same structure as the sample data to avoid syntax issues.

## Publishing & Deploying

To convert your timeline project to HTML, JS and CSS, run `harp compile` from the command line and a `www` directory will be created with all your files contained inside it, which you can publish anywhere.

Here are some popular deploying options:

- [Deploying using the Harp Platform](http://harpjs.com/docs/deployment/harp-platform)
- [Deploying to GitHub Pages](http://harpjs.com/docs/deployment/github-pages)
- [Deploying to Heroku](http://harpjs.com/docs/deployment/heroku)

## Password Protection

Harp supports basic authentication, making it very fast to add password protection to your entire Project Hub.

To add a single password, update the included `_harp.json` file:

```json
{
  "globals": {
    "project_name": "Acme"
  },
  "basicAuth": ["brad_frost:abc123"]
}
```

Now, upon visiting visit [http://localhost:9000/](http://localhost:9000/) in your browser, you will be prompted to enter the correct username (brad_frost) and password (abc123). Multiple username/password combinations are also supported:

```json
{
  "globals": {
    "project_name": "Acme"
  },
  "basicAuth": ["brad_frost:abc123", "client:def456"]
}
```

Note that, because this is a feature of the Harp web server and not HTML, CSS, and JavaScript, the authentication will only work when you are using the [Harp Platform](http://harpjs.com/docs/deployment/harp-platform), or running Harp in production (for example, on [Heroku](http://harpjs.com/docs/deployment/heroku) or [Nodejitsu](http://harpjs.com/docs/deployment/nodejitsu)). Read more about [basic authentication in the Harp documentation](http://harpjs.com/docs/development/basicauth).

## License

MIT