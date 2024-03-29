# Unifig

## What is Unifig

Unifig is a Universal Configuration daemon, managing configuration for multiple applications

## How it works

It works with simple register and request system, where you could have 2 applications that share the same value (eg for a universal color scheme)

## How to use it

Unifig is run in 2 parts, a daemon and a interface for the daemon.
Unifig Interface cannot connect to a remote daemon, only allowing for local access.

## Examples

### Registering and Requesting `Hello`

Key Name: `Hello`

Description: `A hello world example key`

Default: `World`

```py
from unifig import *

unifig.register('Hello', 'A hello world example key', 'World')

value = unifig.get('Hello')

print("Hello, " + value)

```

