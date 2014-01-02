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
- [Overview of project hubs on 24 Ways.](http://24ways.org/2013/project-hubs/)
- [Harp Docs](http://harpjs.com/docs/)

## Getting started

1. Install Harp in your computer
2. Clone this repository
3. Start Harp server
4. Visit http://localhost:9966/ in your browser and follow the instructions

```bash
$ sudo npm install -g harp
$ git clone git@github.com:jorgepedret/harp-project-hub.git
$ harp server harp-project-hub --port 9966
------------
Harp v0.11.0 — Chloi Inc. 2012-2013
Your server is listening at http://localhost:9966/
Press Ctl+C to stop the server
------------
```

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

> Be aware that comas and quotes are important when writing JSON. Follow the same structure as the sample data to avoid syntax issues.


