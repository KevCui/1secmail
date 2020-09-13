# 1secmail

> Use [1secmail](https://www.1secmail.com/) disposable temp mail service from terminal

# Table of Contents

- [Feature](#feature)
- [Dependency](#dependency)
- [How to use](#how-to-use)
  - [Usage](#usage)
  - [Examples](#examples)
- [Run tests](#run-tests)

## Feature

- Fast access to 1secmail service from terminal
- Randomly generating email login
- Easy to remember user name created by Faker
- Simple integration to any CI process due to Bash script

## Dependency

- [cURL](https://curl.haxx.se/download.html)
- [jq](https://stedolan.github.io/jq/)
- [w3m](http://w3m.sourceforge.net/) (optional)
- [faker-cli](https://github.com/lestoni/faker-cli) (optional)

## How to use

### Usage

```
Usage:
  ./1secmail [-i <inbox>|-m <id>|-s]

Options:
  no option        Optional, randamly get an inbox
  -i <inbox>       Optional, get an inbox by its mail address
  -m <id>          Optional, show mail by its id
  -s               Optional, show available domains
  -h | --help      Display this help message
```

### Examples

- Generate a random inbox with `faker-cli`:

```bash
~$ ./1secmail
[]
zoie.brekke@1secmail.net
```

- Generate a random inbox without `faker-cli`:

```bash
~$ ./1secmail
[]
7iaq6u32s@1secmail.com
```

- Get mails in test@1secmail.org inbox:

```bash
~$ ./1secmail -i 'test@1secmail.org'
```

- Show mail 897283223 detail:

```bash
~$ ./1secmail -i 'test@1secmail.org' -m 897283223
```

- Show all available domains:

```bash
~$ ./1secmail -s
```

## Run tests

```bash
~$ bats test/1secmail.bats
```

---

<a href="https://www.buymeacoffee.com/kevcui" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-orange.png" alt="Buy Me A Coffee" height="60px" width="217px"></a>
