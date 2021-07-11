v0.2.0 (in development)
-----------------------
- The log messages displayed for unknown parameters are now at WARNING level
  instead of INFO and include suggestions for what you might have meant
- "git" `vcs` method: `default-tag` will now be honored if the `git describe`
  command fails (which generally only happens in a repository without any
  commits)
- Added an experimental "git-archive" method for determining a version when
  installing from a Git archive
- Added `typing-extensions` as a dependency on Python versions below 3.8

v0.1.0 (2021-07-08)
-------------------
- Add more logging messages
- Changed default version formats to something that doesn't use
  `{next_version}`
- "basic" `tag2version` method:
    - If `regex` is given and it does not contain a group named "`version`,"
      the entire text matched by the regex will be used as the version
    - Added a `require-match` parameter for erroring if the regex does not
      match
- "basic" `write` method: `encoding` now defaults to UTF-8
- New `next-version` methods: `"minor-release"`, `"smallest-release"`, and
  `"null`"
- Replaced `entry-points` dependency with `importlib-metadata`
- Added `tool.versioningit.default-version` for setting the version to use if
  an error occurs
- When building a project from a shallow clone or in a non-sdist directory
  without VCS information, display an informative error message.

v0.1.0a1 (2021-07-05)
---------------------
Alpha release
