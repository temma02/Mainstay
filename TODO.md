# Fix: remove_trusted_issuer does not emit an event

## Steps:

- [x] 1. Edit contracts/engineer-registry/src/lib.rs: Add ISS_RM event publish to remove_trusted_issuer function
- [x] 2. Edit contracts/engineer-registry/src/lib.rs: Add test_remove_trusted_issuer_emits_event test (both edits in parallel)
- [x] 3. Run cargo test in contracts/engineer-registry/ to verify and generate snapshot (tests passed)
- [x] 4. Update TODO.md with completion status
- [x] 5. attempt_completion
