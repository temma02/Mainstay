# Fix Plan

## Issue #333: score increment ignores score_increment config field
- [ ] Modify `submit_maintenance` to use `config.score_increment` instead of `weight`
- [ ] Modify `batch_submit_maintenance` to use `config.score_increment` instead of `weight`
- [ ] Update existing test `test_admin_can_update_score_increment`
- [ ] Add new test `test_score_increment_affects_scoring`
- [ ] Create branch, commit, push

## Issue #334: reset_score admin function does not emit an event
- [ ] Verify `reset_score` emits EVENT_RST_SCR (already does)
- [ ] Add test `test_reset_score_emits_event`
- [ ] Create branch, commit, push

## Issue #335: engineer_history_add does not cap the engineer's asset history list
- [ ] Modify `engineer_history_add` to accept `max_history: u32` and evict oldest
- [ ] Update call sites in `submit_maintenance` and `batch_submit_maintenance`
- [ ] Add test `test_engineer_history_bounded`
- [ ] Create branch, commit, push

## Issue #336: lifecycle contract stores registry addresses in instance storage
- [ ] Move registry address storage to persistent storage
- [ ] Update all registry read/write functions
- [ ] Add test for simulated TTL boundary
- [ ] Create branch, commit, push
# TODO: Fix #318 - register_engineer allows validity_period of 0

- [x] Add `validity_period == 0` guard in `register_engineer`
- [x] Add test `test_register_engineer_zero_validity_rejected`
- [ ] Run `cargo test -p engineer-registry` to verify all tests pass

