# Xplode

A simple Mac OS serivce menu item to quit xcoce and (optionally) move the contents of `~/Library/Developer/Xcode/DerivedData/` to the trash.

Espeically helpful to use before switching branches in git, so Xcode _might_ not puke all over itself if the project file has changes.

## Installation

copy `Xplode.workflow` to `~/Library/Services/`

## Usage

In Xcode:

`Xcode > Services > Xplode`

It _should_ prompt before acutally moivigin things ot the trash.

## Caveats

This assumes you haven't cusomized th location of Derived Data.

## Cusomizing

This is just a silly Automator.app thing so have at it.
