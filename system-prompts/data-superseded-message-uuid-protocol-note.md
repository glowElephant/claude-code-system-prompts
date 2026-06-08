<!--
name: 'Data: Superseded message UUID protocol note'
description: Internal protocol note explaining how supersedes UUIDs mark previously delivered messages as canonical replacements during refusal fallback handling
ccVersion: 2.1.169
-->
@internal Wire uuids of previously-delivered messages that this message replaces (refusal-fallback supersede: server-lane seam merge, or the client-lane retry’s first deliverable content frame). On the client lane the list matches the banner’s retracted_message_uuids exactly and can include tombstoned tool_result frames from the refused leg, not only assistant frames. Evict the named messages on arrival and treat this frame as their canonical replacement. Idempotent with the end-of-turn model_refusal_fallback notice, whose retracted_message_uuids remains the complete audit record for the turn.
