# Precedence Check

**What color is the tagline paragraph?**
The tagline is green (#006400), because of the inline style.

**What color are the other `<p>` tags?**
They are dark red (#8b0000) and italic, from the internal CSS.

**Why?**
1. The external CSS (#555), the internal CSS (#8b0000) and the inline style (#006400) all target the same property, so the one with the highest priority wins.
2. Inline CSS has the highest specificity, so it beats internal CSS, which comes after the external file and wins over it when specificity is equal: inline > internal > external.
3. The tagline gets inline green, and every other `<p>` gets the internal dark red, so the external #555 is overridden everywhere.