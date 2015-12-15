# robot-store
- The robot store git repository was built to demo rapid plugin development for CA CDD using http://hook.io.
- The demo includes a small GitHub plugin which adds an "Update Github issue state" task. The task can be used to close/open issues on github.com.
- The plugin manifest is served by github pages at this url - http://rpm-user.github.io/robot-store/github.json. Use it to register the plugin in CDD. (Changes to the manifest should be done at this [link](https://github.com/rpm-user/robot-store/blob/gh-pages/github.json))
- This "Update Github issue state" task logic is being served by a webhook handler implemented in hook.io. The handler listen to http POST requests at https://hook.io/rpm-user/github-issues and uses GitHub rest api to update the issue.
- You can use [this issue](https://github.com/rpm-user/robot-store/issues/1) to test the plugin task.
- The code executed by the plugin can be viewed [here ](https://hook.io/rpm-user/github-issues/source).
- The logs of the plugin execution can be viewed [here ](https://hook.io/rpm-user/github-issues/logs).

![](https://cloud.githubusercontent.com/assets/14964166/10423929/7f60f950-70d3-11e5-9312-2af20a5956cf.png)

Buy a robot!
