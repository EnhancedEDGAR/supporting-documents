# simplenlg
Java API for Natural Language Generation

Simplenlg is a simple Java API designed to facilitate the generation of Natural Language. It was originally developed at the University of Aberdeen's Department of Computing Science.

Simplenlg is intended to function as a "realisation engine" for Natural Language Generation architectures, and has been used successfully in a number of projects, both academic and commercial. It handles the following

Lexicon/morphology system: The default lexicon computes inflected forms (morphological realisation). We believe this has fair coverage. Better coverage can be obtained by using the NIH Specialist Lexicon (which is supported by simplenlg).
Realiser: Generates texts from a syntactic form. Grammatical coverage is limited compared to tools such as KPML and FUF/SURGE, but we believe it is adequate for many NLG tasks.
Microplanning: Currently just simple aggregation, hopefully will grow over time.

---
## Links to Source Code, Documentation and Discussion 
Google Code(https://code.google.com/p/simplenlg/)

Google Code Source Code(https://code.google.com/p/simplenlg/source/checkout)

Google Code Wiki(https://code.google.com/p/simplenlg/wiki/TableOfContents?tm=6)

Google Forum(https://groups.google.com/forum/#!forum/simplenlg)

----

A SimpleNLG JRuby Gem(https://github.com/efi/simplenlg)
## XML Representation of Text Specifications
Purpose
The SimpleNLG surface realiser produces actual natural language text given an abstract representation of document structure, sentence, phrase and lexical information of the text.
The input to the realiser is called a text specification. A text specification, together with its children (for example, SPhraseSpecs) can be expressed in XML, based on a predefined XML schema that mirrors the relevant parts of the internal structure of a simplenlg specification.
The xmlrealiser is a simplenlg component that takes the XML representation of a text specification, maps it and its children to simplenlg framework objects, invokes a Realiser, and outputs the realisation as text.
The xmlrealiser and the XML schema for text specification provide the following benefits:
• Separates simplenlg from applications using it with a well-defined interface.
• Enables NLG processing in an XML pipeline using XSLT.
• Enables use of automatic code generators of text specification wrapper classes in C++, C#, Java or Visual Basic, making it possible to process inputs and construct the right representations for simplenlg (using the wrapper classes for a specific programming language) and then pass these to simplenlg itself for realization. Thus it also:
• Creates the basis for a simplenlg web service.
• Defines a format for representing text specifications as strings.
• Infrastructure for regression testing


