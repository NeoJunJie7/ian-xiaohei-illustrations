---
name: Add chibi-style LoRA adapter and replace default IP with 小水獭 (xiaoshuita)

This PR adds a LoRA training config and example scripts to produce a cute chibi 小水獭 style (16:9 white background, bold black line art, sparse red/orange/blue annotations). It also replaces occurrences of 小黑/xiaohei with 小水獭/xiaoshuita across repository documentation and prompt templates.

What's included
- LoRA training config tuned for low-VRAM GPUs and demo generator (branch: `add/chibi-style-adapter`).
- Preprocessing utilities to pad training images to 16:9 and optionally generate line-art-enhanced images.
- Style prompt templates and visual QA checklist updated for 小水獭.
- Reference doc: `ian-xiaohei-illustrations/references/xiaoshuita-ip.md` describing the new IP.

Notes
- No private training images are included. Add your examples under `data/chibi_otter/` if you want to train.
- The NOTICE.md attribution to Ian is preserved.

How to test
1. Inspect docs and prompt templates for language updates (search for 小水獭).
2. Run `python demo/generate_chibi.py --lora <path_to_lora_attn_procs> --prompt "holding a shell" --out sample.png` to generate a 16:9 sample.

If you'd like me to attach example outputs or provide a small placeholder dataset, I can update the PR accordingly.

