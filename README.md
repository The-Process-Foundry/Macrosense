# MacroSense

A tool used to add Intellisense, formatting, and debugging to Rust macros (eventually).

Rust macros may contain specialized syntax and symbols that are not part of the standard
grammar. This tool seeks to apply a grammattical formatting based on the name of the macro.

The first use case is to have it use JSX formatting for the Yew based "hmtl!" macro. Standard HTML
formatting would make this much easier to read.

## Questions

Some items I still need to answer about the project:

- Rust webassembly with typescript shim or all typescript?

## TODO

These are the basic items I'm going to work on, mostly in order.y

- DSL/Grammar/AST
  - Make a basic grammar design so users can create their own in settings
- Formatting
  - Rust Macro
  - Simple config options (Add/Ignore Whitespace, splitting long strings, etc.)
  - Integrate with the VS-Code library
- Intellisense
  - Define help in the formatting grammar for better completion/tips
  - Adding external plugins - for example, Tailwind already has an Intellisense
  - Create a derive macro to build a grammar from an AST
- Debugging
  - Add in the results of 'cargo expand' of the selected macro in the peek window
  - Add code highlighting for the errors to the peek window
