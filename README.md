Highlight.js language definition for TON FunC

# FunC - a language grammar for [highlight.js](https://highlightjs.org/)

FunC is a high-level language FunC is used to program smart contracts on TON.

## Usage

Simply include the Highlight.js library in your webpage or Node app, then load this module.

### React

You need to import both Highlight.js and third-party language like Func:

```tsx
import React from 'react'
import hljs from "highlight.js/lib/core";
import { type LanguageFn } from "highlight.js";
import func from "@bakkenbaeck/highlightjs-func";
import "highlight.js/styles/atom-one-light.css"; # your favorite theme

hljs.registerLanguage("fc", func as LanguageFn);

export const CodeComponent: React.FC<{content: string}> = ({content}) => {
    return
    (
        <pre>
            <code
                dangerouslySetInnerHTML={{
                __html: hljs.highlight(content, { language: "fc" }).value
                }}
            />
        </pre>
    )
};
```

## License

Highlight.js is released under the MIT License. See [LICENSE](./License) file
for details.

## Links

- The official site for the Highlight.js library is <https://highlightjs.org/>.
- The Highlight.js GitHub project: <https://github.com/highlightjs/highlight.js>
- Learn more about FunC: <https://docs.ton.org/develop/func/overview>
