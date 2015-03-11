# stackoverflow.questions.1715811
Drupal development and use by professional programmers .. are there specific pitfalls or advantages?

**Background:** Long ago Microsoft Access gained a lot of popularity because you could build pretty powerful desktop database applications with point-and-click ease. It seems like Drupal is now doing the same thing, except for the web.

This is definitely good in some aspects, but it seems to have some drawbacks as well. From the perspective of someone with a few years of Web development experience and programming experience, it seems like Drupal has some quirks that take some getting used to.

**Examples:** 

 - **OOP and Namespaces**: Drupal pretty much re-invents Object Oriented programming with its own internal API, and there does not seem to be much impetus to change that, even though PHP has added built-in support for (its own flavor of) OOP. [See Drupal on OOP][1].

 - **It works for me ...:** Many contrib modules seem to be plagued by use cases that were not initially anticipated by the original author(s). The common response is "well, at least it works for me". This is understandable when developers write something first to solve their own particular issues, and then only later adapt it for others (if funding, personal preferences, and time allow). The problem is "good enough for me" is an incremental approach that does not work well with large-scale development. The result is a combination of solutions that feel "duct taped" together. 

 - **Duplicated Standards:** Drupal seems to also re-invent existing technologies and standards even in cases where there does not seem to be a stylistic or strategic benefit in doing so. For example: 1) New .info files; 2) Deployment tools; 3) Re-creation of PHP language features; 4) Re-creation of code and functionality from established open-source libraries.

(The newly-invented [.info files][2] (used in configs), are used instead of already built-in [INI file][3] format of PHP, or the already-used and published [JSON][4a] or [YAML][4b], for cases where INI is not powerful enough. Another example, in contrib modules at least, you can find lots of hand-made regexes used to parse HTML, instead of already-developed full-fledged HTML parsers. Another example, [Drush][5] appears instead of any already-known [build language][6] out there (**EDIT**: the build language link is not a good one, I meant to emphasize higher-level tools like Rake, Capistrano, Ant, Maven and others, I am assuming Drush is the closest thing.))

 - **Unit testing:** Drupal does not seem to have a strong support for unit testing. Combined with the other factors above, this makes for a challenging environment for those who want to have comprehensive code coverage, especially for cases where Drupal is being used in a work environment with the potential for lots of apps proliferating.

**Question:** If you have some Drupal experience, and also some programming experience (especially if it is in other languages in addition to PHP, with native support for OOP), what are some specific pitfalls or even advantages that you have encountered?

- **Update: (Jul 2, 2013)** Drupal 8 is slated to use YAML instead of the Drupal-specific .info file format (http://en.wikipedia.org/wiki/YAML)

- **Update: (Jul 3, 2013)** Drupal 8 is slated to use the SYMFONY framework which includes native support for Namespaces and Object Orientation.

  [1]: http://drupal.org/node/19964
  [2]: http://drupal.org/node/171205
  [3]: http://en.wikipedia.org/wiki/INI_file
  [4a]: http://en.wikipedia.org/wiki/Json
  [4b]: http://en.wikipedia.org/wiki/YAML
  [5]: http://drupal.org/project/drush
  [6]: http://en.wikipedia.org/wiki/List_of_build_automation_software
