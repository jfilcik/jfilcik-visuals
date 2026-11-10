# jfilcik visuals

A small, static portfolio for interactive visuals.

- [`index.html`](index.html): portfolio placeholder homepage.
- [`content-understanding/index.html`](content-understanding/index.html): Content Understanding benchmark explorer.

GitHub Pages serves the root of `main`. There is no framework, build step, analytics, or content upload feature.

The explorer is an approved chart-only export. Its source SHA-256 is `5e02274c7c90726c54cdd09b29158e995104ab856ee991e78c7921f630d9cd61`. `.gitattributes` preserves its exact bytes. Update it deliberately from a reviewed export rather than editing benchmark data in this hosting repository.

For cross-origin iframe auto-sizing, the parent sends `{type:"cu-explorer-init"}` to this site's exact origin after load. The chart replies to the initiating parent's exact origin with `{type:"cu-explorer-state",ready:true,height:integer}` and reports changed content heights. The parent must validate both the sender's exact origin and the iframe window, and bound accepted heights. The iframe needs `allow-scripts allow-same-origin`; host it on a different origin from its parent. Without parent JavaScript, a fixed-height iframe with normal scrolling and a separate-tab link remains an option.
