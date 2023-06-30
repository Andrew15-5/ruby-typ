# ruby (Typst package)

Usage (<https://github.com/rinmyo/ruby-typ/blob/main/manual.pdf>):

```typst
#import "@preview/ruby:0.9.0": get_ruby

ruby = get_ruby(auto_spacing: false) // Logic from original project
// or
ruby = get_ruby() // Adds missing delimiter around every content/string

#ruby[ふりがな][振り仮名]

// Add space around (already done internally when auto_spacing: true)
#ruby[|きょうりょく|][|協力|]

Treat each kanji as a separate word:
#ruby[とう|きょう|こう|ぎょう|だい|がく][東|京|工|業|大|学]
```

## Notes

Original project is at <https://github.com/rinmyo/ruby-typ>.

`auto_spacing` adds missing delimiter around the `content`/`string` which
then adds space around base text if ruby is wider than the base text.

Problems appear only if ruby is wider than its base text and `auto_spacing` is
not set to `true` (default is `true`).

Although you can open issues or send PRs, I won't be able to always reply
quickly (sometimes I'm very busy).
