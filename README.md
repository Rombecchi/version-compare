# Version compare
Compares two software version numbers  (e.g. "1.7.1" or "1.2b").

Forked from: https://gist.githubusercontent.com/TheDistantSea/8021359


> @param {string} **v1** The first version to be compared.

> @param {string} **v2** The second version to be compared.

> @param {object} **[options]** Optional flags that affect comparison behavior:

- **lexicographical**: (true/[false]) compares each part of the version strings lexicographically instead of naturally; this allows suffixes such as "b" or "dev" but will cause "1.10" to be considered smaller than "1.2".
- **zeroExtend**: ([true]/false) changes the result if one version string has less parts than the other. In this case the shorter string will be padded with "zero" parts instead of being considered smaller.

> @returns {number|NaN}
- **0** if the versions are equal
- a **negative** integer if v1 < v2
- a **positive** integer if v1 > v2
- **NaN** if either version string is in the wrong format
 
 
 ## UPDATE 1.1 (10-04-2018)
- [x] added defaults to lexicographical (false) and zeroExtend (true)
- [x] added alpha/beta versioning as valid parts
- [x] empty v1 or v2 param is assumed as version "0"
- [ ] avoid that lexicographical causing that "1.10" will considered smaller than "1.2"
