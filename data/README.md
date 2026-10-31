# BibleGuess Recent Verse Collections

Recent collections are loaded from `new-verse-collections.json`.

## Add a dated congregation collection

1. Create a JSON file under `data/collections/`, for example `pbb-2026-10-31.json`.
2. Add its metadata to `data/new-verse-collections.json`.
3. Use the exact codeword `NEW VR/ST`. Collections without that codeword are ignored.

Manifest entry:

```json
[
  {
    "id": "pbb-2026-10-31",
    "codeword": "NEW VR/ST",
    "congregation": "PBB",
    "date": "October 31, 2026",
    "title": "PBB October 31, 2026",
    "file": "data/collections/pbb-2026-10-31.json",
    "verseCount": 2
  }
]
```

Collection file:

```json
{
  "verses": [
    {
      "id": "pbb-2026-10-31-1",
      "ref": "Kawikaan 22:6",
      "book": "kawikaan",
      "ch": 22,
      "v": "6",
      "altBook": ["kaw", "pr"],
      "text": "Paste the exact Ang Dating Biblia verse text here.",
      "keyword": "Turuan mo ang bata sa daan",
      "isBeginner": true
    }
  ]
}
```

Each dated collection is isolated. PLAY uses only the selected file for all game modes. STUDY shows the same file's verses and keywords under Recent Topics. Set `isBeginner` to `false` for longer/harder entries; otherwise it is calculated from the verse length.
