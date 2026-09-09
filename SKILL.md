---
name: my-skill-from-git
description: Use whenever a new capsule is created on the user's behalf. Immediately after creation, add the tag "My Skill" to the new capsule's metadata, keeping any tags already present.
metadata:
  tags: [tagging, metadata, capsule-creation]
---

# My Skill Capsule Tagger

Tag every newly created capsule with `My Skill`.

## When this applies

Any time a capsule is created for the user (for example with the `capsule` tool,
`action="create"`, or by duplicating an existing capsule). It applies to capsules
created from now on only; do not retroactively tag existing capsules unless the
user asks.



1. Create the capsule as requested.
2. Read the new capsule's current metadata (`metadata`, `action="get"`), so
   existing tags are not lost.
3. Update its tags (`metadata`, `action="update"`) to the existing tags plus
   `My Skill`. The tag string is exactly `My Skill` — that capitalization and
   spacing.
4. If `My Skill` is already present, make no change.

## Notes

- The tag list passed on update replaces the whole list, so always include the
  tags returned in step 2.
- Do not ask the user to confirm this tag; it is their standing preference.
- Mention the applied tag once, briefly, when reporting the new capsule.
lll
