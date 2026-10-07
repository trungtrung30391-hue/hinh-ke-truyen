# JSON Project Manifest — V6

Mẫu:

```json
{
  "project_title": "Bi an kim tu thap",
  "topic": "Great Pyramid of Giza",
  "platform_mode": "youtube",
  "aspect_ratio": "16:9",
  "total_duration_seconds": 150,
  "visual_lock": {
    "style": "cinematic living-history collage",
    "palette": "warm sand, sepia, dark brown, muted gold",
    "lighting": "dramatic documentary lighting",
    "lens": "35mm cinematic",
    "composition": "single-scene only"
  },
  "subject_lock": {},
  "voice_direction": {},
  "music_direction": {},
  "scenes": [
    {
      "scene_number": 1,
      "filename": "01-mo-dau.png",
      "start_time": "00:00:00",
      "end_time": "00:00:08",
      "duration_seconds": 8,
      "stage": "hook",
      "narration_vi": "...",
      "image_prompt_en": "...",
      "video_motion_prompt_en": "...",
      "sound_effects": ["desert wind"],
      "transition": "slow fade",
      "voice_cue": "mysterious, calm"
    }
  ]
}
```

Yêu cầu:
- JSON parse được.
- Không comment.
- Không trailing comma.
- Timeline phải khớp.
