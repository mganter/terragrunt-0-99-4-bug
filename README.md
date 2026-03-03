# How to bug?

1. use terragrunt version 0.99.3

```sh
> tgswitch
✔ 0.99.3 *recent
Installing terragrunt at /Users/<user>/bin
Switched terragrunt to version "0.99.3" 
```

2. terragrunt --log-level=debug stack generate

```sh
> terragrunt --log-level=debug stack generate
12:04:17.928 DEBUG  Terragrunt Version: 0.99.3
12:04:17.929 DEBUG  using cache key for version files: r01AJjVD7VSXCQk1ORuh_no_NRY
12:04:17.929 DEBUG  Running command: tofu -version
12:04:17.929 DEBUG  Engine is not enabled, running command directly in .
12:04:17.951 DEBUG  tofu version: 1.11.5
12:04:17.951 DEBUG  Auto provider cache dir enabled: TF_PLUGIN_CACHE_DIR=../../../../Library/Caches/terragrunt/providers
12:04:17.954 DEBUG  Generating stack level 0 with 2 files
12:04:17.955 DEBUG  Reading Terragrunt stack config file at ./stacks/test/terragrunt.stack.hcl
12:04:17.955 DEBUG  Reading Terragrunt stack config file at ./non-prod/dev/terragrunt.stack.hcl
12:04:17.960 DEBUG  Running command: git rev-parse --show-toplevel
12:04:17.960 DEBUG  Command output will be suppressed.
12:04:17.960 DEBUG  Running command: git rev-parse --show-toplevel
12:04:17.960 DEBUG  Command output will be suppressed.
12:04:17.975 DEBUG  git show-toplevel result: .
12:04:17.975 DEBUG  git show-toplevel result: .
12:04:17.976 INFO   Generating stack test from ./non-prod/dev/terragrunt.stack.hcl
12:04:17.976 DEBUG  Generating: test (./stacks/test) to ./non-prod/dev/.terragrunt-stack/test
12:04:17.976 INFO   Generating unit test from ./stacks/test/terragrunt.stack.hcl
12:04:17.976 DEBUG  Generating: test (./units/test) to ./stacks/test/.terragrunt-stack/test
12:04:17.979 DEBUG  No values to write in ./stacks/test/.terragrunt-stack/test
12:04:17.990 DEBUG  No values to write in ./non-prod/dev/.terragrunt-stack/test
12:04:17.993 DEBUG  Adding 1 new stack files to topology graph
12:04:17.993 DEBUG  Stack ./non-prod/dev/.terragrunt-stack/test/terragrunt.stack.hcl (level 1) is child of ./non-prod/dev/terragrunt.stack.hcl (level 0)
12:04:17.993 DEBUG  Generating stack level 1 with 1 files
12:04:17.993 DEBUG  Reading Terragrunt stack config file at ./non-prod/dev/.terragrunt-stack/test/terragrunt.stack.hcl
12:04:18.007 DEBUG  Running command: git rev-parse --show-toplevel
12:04:18.007 DEBUG  Command output will be suppressed.
12:04:18.020 DEBUG  git show-toplevel result: .
12:04:18.021 INFO   Generating unit test from ./non-prod/dev/.terragrunt-stack/test/terragrunt.stack.hcl
12:04:18.021 DEBUG  Generating: test (./units/test) to ./non-prod/dev/.terragrunt-stack/test/.terragrunt-stack/test
12:04:18.022 DEBUG  No values to write in ./non-prod/dev/.terragrunt-stack/test/.terragrunt-stack/test
````

3. use terragrunt version 0.99.4

```sh
> tgswitch
✔ 0.99.4 *recent
Installing terragrunt at /Users/<user>/bin
Switched terragrunt to version "0.99.4"
```

4. terragrunt --log-level=debug stack generate

```sh
> terragrunt --log-level=debug stack generate
12:06:15.084 DEBUG  Terragrunt Version: 0.99.4
12:06:15.087 DEBUG  using cache key for version files: r01AJjVD7VSXCQk1ORuh_no_NRY
12:06:15.087 DEBUG  Running command: tofu -version
12:06:15.087 DEBUG  Engine is not enabled, running command directly in .
12:06:15.109 DEBUG  tofu version: 1.11.5
12:06:15.109 DEBUG  Auto provider cache dir enabled: TF_PLUGIN_CACHE_DIR=../../../../Library/Caches/terragrunt/providers
12:06:15.113 WARN   No stack files found in . Nothing to generate.
```
