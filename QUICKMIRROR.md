# QuickMirror maintenance branch

Remote: git@gitee.com:Barryda/idevice.git
Branch: codex/quickmirror-ios
Upstream base: e98264c4194e6980173c576ac79a58adce95492b

Bounded USBMux, HTTP, HTTP/2 and XPC parsing; tunnel validation; AMFI/Cryptex/TSS fixes; independent HID feature and async service reads.

This fork is consumed by quick-desktop as a pinned Git submodule. Changes are
committed directly; builds do not apply source patches or follow branch tips.
The two forks must be checked out as sibling directories named idevice and
jktcp. idevice/idevice/Cargo.toml resolves jktcp through ../../jktcp.

Build the product with its locked dependency graph using
`cargo build --locked --manifest-path src/ios/services/Cargo.toml` from
quick-desktop. Keep build output and additional validation artifacts outside
source checkouts via CARGO_TARGET_DIR.

The initial fork commit migrates QuickMirror's previously validated production
changes with AI assistance. Upstream license notices are preserved.
