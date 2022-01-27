# Xplode

A simple Mac OS service menu item to quit Xcode, purge your local SPM cache, and (optionally) move the contents of `~/Library/Developer/Xcode/DerivedData/` to the trash.

Especially helpful to use before switching branches in git, so Xcode _might_ not puke all over itself if the project file has changes.

## Installation

copy `Xplode.workflow` to `~/Library/Services/`

## Usage

In Xcode:

`Xcode > Services > Xplode`

It _should_ prompt before actually moving things to the trash.

## Caveats

This assumes you haven't customized the location of Derived Data.

## SPM Cache

From thew Xcode 12.5 release notes:

> Swift Package Manager caches package dependencies on a per-user basis, which reduces the amount of network traffic and increases performance of dependency resolution for subsequent uses of the same package. If needed, you can disable cache use in xcodebuild by using the new -disablePackageRepositoryCache flag. (72204929)

This cache appears to be located in `~/Library/Caches/org.swift.swiftpm/`. Xplode moves this to the trash without prompting, because it's just a cache.

## Customizing

This is just a silly Automator.app thing so have at it.
