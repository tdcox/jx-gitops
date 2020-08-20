## jx-gitops image

Updates images in the kubernetes resources from the version stream

### Usage

```
jx-gitops image
```

### Synopsis

Updates images in the kubernetes resources from the version stream

### Examples

  # modify the images in the content-root folder using the current version stream
  jx-gitops image
  # modify the images in the ./src dir using the current dir to find the version stream
  jx-gitops image --source-dir ./src --dir .

### Options

```
  -d, --dir string                  the directory that contains the jx-requirements.yml (default ".")
  -h, --help                        help for image
  -k, --kind stringArray            adds Kubernetes resource kinds to filter on. For kind expressions see: https://github.com/jenkins-x/jx-helpers/tree/master/docs/kind_filters.md
      --kind-ignore stringArray     adds Kubernetes resource kinds to exclude. For kind expressions see: https://github.com/jenkins-x/jx-helpers/tree/master/docs/kind_filters.md
  -s, --source-dir string           the directory to recursively look for the *.yaml files to modify (default "content-root")
      --version-stream-dir string   the directory for the version stream. Defaults to 'versionStream' in the current --dir
  -c, --version-stream-ref string   the git ref (branch, tag, revision) of the version stream to git clone. If not specified it defaults to the value in the jx-requirements.yml
  -n, --version-stream-url string   the git clone URL of the version stream. If not specified it defaults to the value in the jx-requirements.yml
```

### SEE ALSO

* [jx-gitops](jx-gitops.md)	 - GitOps utility commands

###### Auto generated by spf13/cobra on 20-Aug-2020