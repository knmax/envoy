# 文件系统标志

Envoy supports file system “flags” that alter state at startup. This is used to persist changes between restarts if necessary. The flag files should be placed in the directory specified in the [flags_path](../configuration/overview/v1_overview.md#config-overview-flags-path) configuration option. The currently supported flag files are:

- drain

  If this file exists, Envoy will start in HC failing mode, similar to after the [`POST /healthcheck/fail`](admin.md#post--healthcheck-fail)command has been executed. 