# Definitions of Technical Terms Used
There are a number of terms used that refer to specific modules, objects, or
other technical elements.

## Neon Technologies
Some commonly used Neon technologies are described here.

### Neon Core
Neon Core refers specifically to the collection of "core" Neon modules.
More information about these modules can be found in the 
[Core Modules](https://neongeckocom.github.io/neon-docs/neon_core/index) section
of this documentation.

### Neon OS
Neon OS (and Neon AI OS) refers to operating systems (sometimes referred to as 'images') that
include Neon Core and other software. More information can be found in the
[Neon OS](https://neongeckocom.github.io/neon-docs/neon_os/) section of this
documentation.

### Diana
Diana (Device Independent API for Neon AI) is a collection of microservices that
run on a backend server. More information is available 
[on GitHub](https://github.com/neongeckocom/neon-diana-utils).

### Mana
Mana (Messagebus Application for Neon AI) is a Commandline Application for 
interacting with services on the 
[Messagebus](https://neongeckocom.github.io/neon-docs/neon_core/messagebus). 
More information is available
[on Github](https://github.com/neongeckocom/neon-mana-utils)

### Iris
Iris (Interactive Relay for Intelligence Systems) is a Python module and
Commandline Application for interacting with services on the MQ Bus.
More information is available 
[on Github](https://neongeckocom.github.io/neon-docs/neon_core/index).

## Operations Documentation
The Operations Documentation and other documents discussing code organization or
processes use some specific terms to refer to different kinds of modules.

### Plugin
Refers to a module that may be replaced by an equivalent module. These will usually 
extend a class from [ovos-plugin-manager](https://github.com/openvoiceos/ovos-plugin-manager).

### Skill
Refers to a class that extends `MycroftSkill`, `OVOSSkill`, or `NeonSkill`. A `skill` is a subset of a `plugin`.
For the purposes of the operations documentation, a skill is distinctly different
from a plugin.

### Service
Refers to a module that runs as a standalone service. This often includes a Docker
container that runs the service. Many plugins may be run as a standalone service,
but for the purposes of the operations documentation those are considered plugins
and not services.
> For example, `neon-audio` is a service but `neon-tts-plugin-coqui` is not. Even
  though the plugin has a container with a web UI, it is a TTS plugin first.

### Library
Refers to Python packages that do not expose any services or implement a specific
plugin. These are often dependencies of many plugins and services.

## Neon (and OVOS and Mycroft) Core
Some commonly used terms in the context of Neon (and other) Cores. See also
the [OVOS Docs](https://openvoiceos.github.io/community-docs/glossary/) and
[Mycroft Docs](https://mycroft-ai.gitbook.io/docs/about-mycroft-ai/glossary).

### Module
"Module" is sometimes used to refer to a 
[Neon Core Service](https://neongeckocom.github.io/neon-docs/neon_core/index).
Note that "module" is also defined 
[in Python](https://docs.python.org/3/tutorial/modules.html#more-on-modules).

### Utterance
The text associated with something said or typed in by a user.

### Intent
The calculated meaning of an [utterance](#utterance).

### Plugin
A Python package that is optional and interchangeable. More information
is available in the [OVOS Plugin Manager Documentation](https://openvoiceos.github.io/community-docs/OPM/).

### Skill
An object that extends the `MycroftSkill` class. Skills generally
provide some [intent](#intent) handling, but are not required to.
> Note that a Python package containing a skill object is also referred to as a 'skill'

### Message
A `message` is a specific object class defined in the 
[mycroft-bus-client](https://github.com/MycroftAI/mycroft-messagebus-client#message).

## Skills
Some commonly used terms in the context of [skills](#skill).

### Intent Handler
A skill object `method` that is associated with an [intent](#intent).

### Skill Settings
A skill-specific settings object (`MycroftSkill.settings`).

### vocab (voc)
Structured plaintext files that define a skill's known vocabulary for parsing
user inputs ([utterances](#utterance))

### dialog
Structured plaintext files that define a skill's responses.

### regex (rx)
Structured plaintext files that define 
[regex parsing](https://docs.python.org/3/howto/regex.html) for a skill.