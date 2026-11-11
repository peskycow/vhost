# Local vhost changes

Based on the crates.io vhost 0.16.0 release. Original source notices and licenses remain intact. The opt-in `incremental` feature shares the original request dispatcher with a bounded nonblocking frame/reply state machine. It owns ancillary descriptors with atomic CLOEXEC, preserves partial reads/writes, retains at most one frame and reply, and negotiates only the protocol operations supported by this mode. The original blocking API is unchanged.

Peer authentication, memory FD seals, mapping limits and replacement policy belong to the caller's backend callbacks. Aspect Remote enforces these in its reactor-local Control before mapping memory. The vhost-user-backend crate is unchanged from its public release.
