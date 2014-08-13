# Heroku Buildpack: Go

This is a [Heroku buildpack][buildpack] for [Go][go].

Place a .gopath file in the root directory containing the GOPATH (relative to the root).
All binaries will be copied to the bin/ which can then be referred from the Profile.
Optionally, place a .gover file containing the desired go version. The default is '1.3.1'.


The buildpack adds a `heroku` [build constraint][build-constraint],
to enable heroku-specific code. See the [App Engine build constraints article][app-engine-build-constraints]
for more.

## Hacking on this Buildpack

To change this buildpack, fork it on GitHub. Push
changes to your fork, then create a test app with
`--buildpack YOUR_GITHUB_GIT_URL` and push to it. If you
already have an existing app you may use `heroku config:add
BUILDPACK_URL=YOUR_GITHUB_GIT_URL` instead of `--buildpack`.

[go]: http://golang.org
[buildpack]: http://devcenter.heroku.com/articles/buildpacks
[build-constraint]: http://golang.org/pkg/go/build/
[app-engine-build-constraints]: http://blog.golang.org/2013/01/the-app-engine-sdk-and-workspaces-gopath.html
