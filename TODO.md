# TODO: Fix #317 - renew_credential minimum validity period

- [x] Read and understand contract code and tests
- [x] Add `InvalidValidityPeriod = 13` to `ContractError` enum
- [x] Add `MIN_VALIDITY_PERIOD: u64 = 86_400` constant
- [x] Add guard in `renew_credential` rejecting `new_validity_period < MIN_VALIDITY_PERIOD`
- [x] Add test `test_renew_credential_short_validity_rejected`
- [ ] Run `cargo test` to verify all tests pass

