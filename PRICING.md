# API pricing · 2026-10-22

| Model / 模型 | Preset / 参数 | API pricing | Case / 本次案例 |
|---|---|---|---|
| gpt-image-2 | n=1, size=1:1, resolution=1K, metadata={'resolution': '1K'} | $0.015/image | $0.015 quote |
| gpt-image-2.5-flare | n=1, size=1:1, metadata={'resolution': '1K'}, quality=high | $0.0225/image | $0.0225 quote |
| MiniMax-H3-Max-Turbo | duration=5, resolution=480P, aspect_ratio=16:9 | $0.025/s | $0.125 actual; 5.18s; $0.024131/s observed |

Token-metered rates use actual tokens; the observed $/s is this case’s settled cost divided by decoded MP4 duration, not a fixed future rate. Quotes are same-Key prices dated 2026-10-22, not confirmed charges. The client rechecks pricing before a paid submission.
