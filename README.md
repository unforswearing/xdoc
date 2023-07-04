
# xdoc

 A very quick and very dirty documentation tool a la `jsdoc` for shell scripts

## About

This tool was created as a way to add documentation to shell scripts without the 
need for as many options as `shdoc` or `literate`. This tool scans for a few tags
used to format the structure of the doc. Otherwise the rest of the content can be
written in a limited version of markdown. The output is plain markdown that can 
be used as a README.

## Usage

`xdoc input.bash README.md`  

## Options

Options for this script are the available tags, which include **@title**, **@brief**, **@description**
**@install**, **@usage**, and **@options**.

Note the following limitations:  
- **@title** and **@brief** must be one line. 

-  **@description**, **@install**, **@usage**, and **@options** require multiline strings wrapped in 
square brackets. 

- List items must have a blank line after each item or section of items

#### Description of options

**@title**
- The title of your project, must be one line

**@brief**
- A short summary of your project, must be one line

**@description**
- A longer explanation of your project. 
- Multiline must be wrapped in square brackets

**@install**
- Installation instructions
- Multiline must be wrapped in square brackets

**@options**
- A list of available options
- Multiline must be wrapped in square brackets


