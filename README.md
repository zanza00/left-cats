left cats
=========

A scala implementation of the [left-pad javascrpit library](https://www.npmjs.com/package/left-pad)

I was inspired by [this article(http://arstechnica.com/information-technology/2016/03/rage-quit-coder-unpublished-17-lines-of-javascript-and-broke-the-internet/) to port this to Scala.

This implementaion will let you pad arbitrary F[A] structures with As
as long as you have implicit cats.Foldable and cats.Alternative instances.

example usage:

    scala> import left.cats._, LeftPad._

    scala> LeftPad[String,Char].leftPad("asdf")(10, ' ') 
    res0: String = "      asdf"

Of course, it builds in scalaJS as well.
