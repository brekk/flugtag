# flugtag

ad-hoc, nestable, relatable tags

Some rules about tags:

1. *Tags* are non-empty caseless* string lists, e.g.: `Tag(["shop", "bakery", "Tartine"])` &mdash; *A tag can have cased text but the case of the text is not used in any automatic sorting or comparison
2. Each index is a *Scope*
   a. The first *Scope* is the __Root__ *Scope*
   b. The last *Scope* is the __Focus__ *Scope*
3. A *Band* is a single-*Scope* Tag
4. Other *Tags* are considered siblings if the given *Tags* share a __Root__ *Scope*
5. The overlap between *Tags* denotes their affinity

    a = Tag(["shop", "bakery", "Tartine"])
    b = Tag(["shop", "exotic", "Paxton Gate"])

These two *Tags* have the same *Band*, "shop", and it's in the same place, so they have a stronger affinity than

    c = Tag(["airport", "shop", "Peetz", "Drip Coffee"])

since `a` and `b` have the same __Root__ *Scope* and length, they have the same affinity to `c`


