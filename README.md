# grunt-iron-worker

A grunt plugin to manage your iron workers. It currently just uses the iron.io CLI. Therefore you need to `gem install iron_worker_ng`. For more details or troubleshooting refer to [http://dev.iron.io/worker/reference/cli/](http://dev.iron.io/worker/reference/cli/).

## Getting Started
This plugin requires Grunt `~0.4.0`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-iron-worker --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-iron-worker');
```




## Iron Worker Task
_Run this task with the `grunt ironworker` command._

Task targets, files and options may be specified according to the grunt [Configuring tasks](http://gruntjs.com/configuring-tasks) guide.

### Options

TODO: Fill this guy in

### Usage Examples

```js
ironworker: {
  options: {
    worker: '<%= pkg.name %>.worker',
    payloadFile: 'config.json',
    payload: {},
    projectId: 'xxxxxxx'
    environment: 'Production'
  },
  run: {},
  upload: {
    name: 'foo',                    // Override code name
    concurrency: 1,                 // Max number of concurrent users
    retries: 1,                     // Max number of auto retries on task fail
    retriesDelay: 1,                // Delay between auto retry
    host: 'http://example.com',
    async: false,                   // Don't wait for package build
    fullRemoteBuild: false          // Do a complete remote rebuild
  },
  queue: {
    priority: 0,          // 0|1|2
    timeout: 3600,        // In seconds
    delay: 5,             // In seconds
  },
  schedule: {
    priority: 0,          // 0|1|2
    timeout: 3600,        // In seconds
    delay: 5,             // In seconds
    start: new Date(),    // ISO Date 2013-01-01T00:00:00-04:00
    end: new Date(),      // ISO Date 2013-01-01T00:00:00-04:00
    runTimes: 0,          // Run every n times
    runEvery: 0,          // Run every n seconds
  }
}
```


## Release History

 * 2013-04-03   v0.0.1   First Version. Woo!