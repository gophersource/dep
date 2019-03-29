<img src="docs/assets/DigbyShadows.png" width="150px" align="right" />

# GopherSource: dep

This is a fork of the [upstream dep repository][dep-git] as part of the
[GopherSource][gs] project where the community can try out changes to the 
`go` commands, a.k.a. the "toolchain", and provide feedback.

We are experimenting with integrating dep with the go toolchain, and
improving the user experience of dep at the same time:

* Any dependency, even transitive, can be controlled with `[constraint]`.
* NoGoCode errors are only warnings, making it easier to require tools.
* Retroactively apply -v when a solve error occurs, so you don't have to run it 
  all over again.
* Listen to a key combo to show the logs collected from the item above, so that
  when it's taking a long time, you can see what's going on.
* Track who introduced a dependency, so that when a solve fails, you can see
  a list of who wanted it, and at which versions.
* Support talking with Athens proxies. We can use that to protect against all
  of the problems that Athens solves, in addition to generally improving the 
  performance of `dep ensure`.

## Installation

```
go get -u github.com/gophersource/dep/cmd/dep
```

### Contributing

We are actively seeking new contributors and ideas at all times! See our
[Contributing Guide][contributing] for how to get started.

We want to let you know that we follow a general [philosophy][philosophy] in how
we work together, and we'd really appreciate you getting familiar with it before
you start.

[gs]: https://gophersource.com
[dep-git]: https://github.com/golang/dep
[setup]: https://gophersource.com/setup
[contributing]: ./CONTRIBUTING.md
[philosophy]: https://gophersource.com/philosophy/