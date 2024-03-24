> [!NOTE]
> Currently doing early-stage investigative work for this project.

# ankiml
The **anki markup language** is a markup language that can be interpreted to
generate [Anki](https://apps.ankiweb.net/) decks, allowing automatic Anki card
generation.

This repository contains the specification for ankiml along with tests that
can be run against the specification, and reference implementations for parsers
and compilers that can be used to compile `.ankiml` files to [packaged Anki
decks](https://docs.ankiweb.net/exporting.html#packaged-decks).

## Motivation
In broad terms, this effort should enable *anki-as-code*. In other words this
project should enable the expression of Anki decks in plaintext. The benefits of
a plaintext format include but are not limited to
- easier integrations with version control tools,
- programmatic generation of Anki decks, and
- interoperability with existing IDE's and text editors.

Ankiml is to Anki decks as markdown is to HTML.

## Goals
These goals will guide the development of the Anki markup language.
1. **Compatible**: Conversion between (to and from) `.apkg` and ankiml shall be
possible.
2. **Readable**: ankiml shall be easy to read and write by a human.
3. **Extendable**: ankiml shall be extendable to interop Anki's plugin
ecosystem.
4. **Writeable**: Writing ankiml shall feel *good*.
5. **Superset CommonMark**: Ankiml shall be a superset of [CommonMark
](https://commonmark.org/).

## Example use case
This is a hypothetical use case that I hope ankiml will eventually fulfill.
> Greg is a note taking and knowledge management enthusiast. He takes notes in
ankiml. Greg's notes are hosted on a github repository, and he uses a github
action that validates his ankiml notes and compiles them to an Anki package,
which is then uploaded to and synchronized against his Anki server.
