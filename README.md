# what
Making BOSH packages for apt and other library / debian package dependancies is notoriously painful and can often result in nearly drowning in sea of your own salty tears. I know. I've been there.

The `bosh-gen`CLI helps a little with this ... sorta ... Unfortunately while it helps in some ways, it doesn't go far enough for packages which need to be configured, and doesn't seem to cache everything required; opting for using `dpkg` to [extract the packages downloaded from apt](https://github.com/cloudfoundry-community/bosh-gen/blob/c96819a102b50ede13717f2aa621b796d92e9892/lib/bosh/gen/generators/package_apt_generator.rb) but doesn't run any configuration of those packages.

This utility hopes to assist in baking these types of dependancies into a package, and allowing the installation and configuration of all the libraries required in a way that makes both BOSH and apt happy; and in turn makes you happy and avoids the aforementioned sea of salty tears.

# Bundling apt dependancies

...
