```bazel
bazel build //browserclient:build
```

#Error
```
~/Desktop/angular_bazel_architect_2 % bazel build //browserclient:build
INFO: Invocation ID: 355172f6-90e8-4135-9239-75bbb53c7f30
INFO: Analyzed target //browserclient:build (1043 packages loaded, 75010 targets configured).
INFO: Found 1 target...
ERROR: /Users/yhierts/Desktop/angular_bazel_architect_2/browserclient/BUILD.bazel:28:10: Action browserclient/build failed: (Exit 3): architect.sh failed: error executing command bazel-out/host/bin/external/npm/@angular-devkit/architect-cli/bin/architect.sh frontend:build '--outputPath=bazel-out/darwin-fastbuild/bin/browserclient/build' ... (remaining 1 argument(s) skipped)

Use --sandbox_debug to see verbose messages from the sandbox
Workspace configuration file (angular.json, .angular.json, workspace.json, .workspace.json) cannot be found in '/private/var/tmp/_bazel_yhierts/5f2ad52dfea8dd1547096fb54025b139/sandbox/darwin-sandbox/1/execroot/angular_bazel_architect' or in parent directories.
Target //browserclient:build failed to build
Use --verbose_failures to see the command lines of failed build steps.
INFO: Elapsed time: 117.506s, Critical Path: 28.76s
INFO: 9 processes: 9 internal.
FAILED: Build did NOT complete successfully
```

# Current issues
* lint not working
* files not compilable, means something happens, but result files cannot be found
* serve is not working
* always (90% of cases) npm tries to refetch node_modules again and again even nothing was changed
