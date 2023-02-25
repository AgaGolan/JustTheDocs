---
title: Markdown
layout: default
nav_order: 2
has_children: true
---



**Why it is usually a bad idea to copy localization resources or xml/html fragments to Excel?**

1. Because they fit to CAT tools. Common CAT tools can handle common
content useful for UI resources, web pages or documentation. If you use any $variables, CAT protects them from translation. Excel doesn't.
2. Because translators use a lot of context to translate the
resources properly. JSON or YAML files *hide* a lot of useful information as comments, key IDs, or derive it from the sequence of strings in file (e.g. when button labels are grouped together). Don't move strings to Excel - you can strip the translatable content out of the context.
3. Because after copy/paste to Excel you can add two steps: sort
the strings alphabetically and remove duplicates. Don’t do it - you can strip the strings further off their natural context (see above). You can erase the good redundancy which can translate the same word in different contexts.
4. Because you can trigger an error - incomplete export or import, code page issues, mixing up Polish with Portuguese or Chinese Simplified with Traditional. Don't try this.

**So, how to translate the resources?**

1. First, try to export them from your CMS / programming tool in primal form. Send a sample export to an experienced Translator or LSP and ask them if the format is CAT-friendly.
2. If it's not, check the possibilities of other export formats available from your tool: JSON, PO, XLIFF?
3. Use Excel (or CSV) only if none of the above works.  
How to do it right:

- Include keys and comments along with translatable text - as separate columns and rows(!);
- Do not sort – don't change the content structure;
- Do not exclude duplicates –  Translators use them too!
- Check for errors like strings broken into multiple rows, currency converted to date, etc.