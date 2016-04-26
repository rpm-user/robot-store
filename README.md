# CDD GitHub plugin demo
- This small demo was built as an example for rapid CDD plugin development using [hook.io](http://hook.io/docs).
- The demo includes a small CDD GitHub plugin which adds an "Update Github issue state" task. The task can be used to close/open issues on github.com (i.e. issues in this project).
- The plugin manifest is served by github pages at this url - http://rpm-user.github.io/robot-store/github.json. Use it to register the plugin in CDD. (Changes to the manifest should be done at this [link](github.json) on the gh-pages branch)
- This "Update Github issue state" task logic is being served by a webhook handler implemented in hook.io. The handler listen to http POST requests to the following url: `https://hook.io/rpm-user/github-issues` and uses GitHub rest api to update the issue.
- You can use [this GitHub issue](https://github.com/rpm-user/robot-store/issues/1) to test the plugin task, by using the following inputs for the task:
  - Endpoint properties
    - GitHub user: rpm-user
    - Repository name: robot-store
    - Authorization: Trust me
  - Task properties
    - Issue id: 1
    - Issue status (closed/open): closed
- The code executed by the plugin (on hook.io) can be viewed [here ](https://hook.io/rpm-user/github-issues/source). [(static copy)](github_plugin_hook_1_0.js)
- The logs of the plugin execution can be viewed [here ](https://hook.io/rpm-user/github-issues/logs).

![](https://cloud.githubusercontent.com/assets/14964166/10423929/7f60f950-70d3-11e5-9312-2af20a5956cf.png)

test2
