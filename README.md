# mfp-cli-ext

Extensions for working with the [IBM MobileFirst Platform Foundation Command
Line Interface](https://developer.ibm.com/mobilefirstplatform/install/#clui).
Not official.

# General Philosophy

`mfp-cli-ext` builds on top of and enhances the standard mfp tool provided by
the IBM MobileFirst Platform Foundation CLI. You can type:

`mfp-cli-ext command variousparams`

If `mfp-cli-ext` doesn't recognise the command you provided, it will pass it
straight through to the standard `mfp` tool. However, `mfp-cli-ext` adds some
extra commands which `mfp` doesn't know. These include:

* `native-ide environmenttype`: Assuming you are within a Worklight
  application inside a Worklight project, this will open the native IDE tool
  for that type of environment (only supports XCode so far).

## Examples

You could create a Worklight project, add an application, and then open XCode
in the following fashion:

* `mkdir /tmp/somedirectory && cd /tmp/somedirectory`
* `mfp-cli-ext create` (create a new project called MyProject)
* `cd MyProject`
* `mfp-cli-ext add hybrid` (create a new app called MyApp)
* `cd apps/MyApp`
* `mfp-cli-ext add environment iphone` (create a new app called MyApp)


