<center>
<img src="https://www.doxygen.nl/images/doxygen.png" alt="Doxygen"/>
</center>

# Notes on Doxygen

## Table Of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Getting Started](#getting-started)
  - [Generate Config File](#generate-doxygen-config-file)
  - [Documenting The Code](#documenting-the-code)

## Introduction

Doxygen is a documentation generator and static analysis tool for software source trees. When used as a documentation generator, Doxygen extracts information from specially-formatted comments within the code. When used for analysis, Doxygen uses its parse tree to generate diagrams and charts of the code structure.[^1]

Doxygen is the de facto standard tool for generating documentation from annotated C++ sources, but it also supports other popular programming languages such as C, Objective-C, C#, PHP, Java, Python, IDL (Corba, Microsoft, and UNO/OpenOffice flavors), Fortran, and to some extent D. Doxygen also supports the hardware description language VHDL.[^2]

## Installation

Ubuntu

    sudo apt-get install doxygen

Fedora / Centos

    sudo yum install doxygen

## Getting Started

1. ### Generate Doxygen Config File

    To simplify the creation of a configuration file, doxygen can create a template configuration file for you.

        doxygen -g <config_filename>

   ```<config_filename>``` is the name of the configuration file. If you omit the file name, a file named Doxyfile will be created.

        doxygen -g -s <config_filename>
    If ```-s``` is specified the comments of the configuration items in the config file will be omitted.

2. ### Documenting the code

    A special comment block is a C or C++ style comment block with some additional markings, so doxygen knows it is a piece of structured text that needs to end up in the generated documentation.

    There are several ways to mark a comment block as a detailed description but

    You can use the Javadoc style, which consist of a C-style comment block starting with two *'s, like this:

        /**
         * ... Describe your code ...
         */

    **Putting documentation after members**

        int var; ///< Brief description after the member

3. ### Examples

        class Nothing{

            /**
            * @brief I also don't know what is this
            * @param nameOfNothing take name of user
            * @return int Its return integers 
            */
            int doNothing(string nameOfNothing){
                // Do nothing logic implementation goes here;

                return integer;
            }
        }

[^1]: <https://en.wikipedia.org/wiki/Doxygen>
[^2]: <https://www.doxygen.nl/>
