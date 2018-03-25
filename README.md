# Lift CMS Site

The Lift CMS site is statically generated on push using https://telegr.am/ and
lives at https://liftweb.net/ . The underlying engine behind Telegram is the
[hoisted](https://github.com/hoisted/hoisted) static site generator, which is
built on top of Lift itself.

## Generating the Site

If you want to work on the site yourself, you can download [the hoisted.jar
file from telegram](https://howto.telegr.am/download/hoisted.jar) and then
run, from the root directory of this repository:

```bash
$ java -jar /path/to/hoisted.jar site compiled
```

You'll then get a `compiled` directory with the HTML version of the site!

## Releasing a New Version

There are a few steps that are currently manual when a new Lift release goes
out, including creating an entry for the Lift version at `happening/` and
building and updating the API docs in `api/`.

## Adding News

For now, adding news is just a matter of adding an appropriate file to
`happening/`. “Appropriate” requires cloning an existing `.cms.xml` file
and changing the bits that seem relevant. This will be more straightforward
soon when Markdown support is merged.

## Format

Currently all the documents in the site are `.cms.xml` files, which are files
designed for hoisted to consume. However, hoisted will also happily work with
Markdown files, as long as they're named `.md`. There are still a few hurdles
before markdown files will be immediately usable for happenings.
