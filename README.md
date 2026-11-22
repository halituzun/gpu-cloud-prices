# Cloud GPU rental prices

Starting hourly prices for renting NVIDIA GPUs in the cloud, plus a daily price index per GPU model. The data comes from the live catalog at [CoreHu](https://corehu.com/gpu-prices), which bills per second in USD.

## Popular GPUs (2026-11-22)

| GPU | Memory per GPU | From, per GPU per hour |
|---|---|---|
| [RTX 3090](https://corehu.com/gpus/rtx-3090) | 24 GB | $0.26 |
| [RTX 4090](https://corehu.com/gpus/rtx-4090) | 24 GB | $0.67 |
| [RTX 5090](https://corehu.com/gpus/rtx-5090) | 32 GB | $0.78 |
| [L40S](https://corehu.com/gpus/l40s) | 48 GB | $0.99 |
| [RTX A6000](https://corehu.com/gpus/rtx-a6000) | 48 GB | $0.81 |
| [A100 SXM4](https://corehu.com/gpus/a100-sxm4) | 40 GB | $1.00 |
| [A100 PCIE](https://corehu.com/gpus/a100-pcie) | 40 GB | $0.67 |
| [H100 SXM](https://corehu.com/gpus/h100-sxm) | 80 GB | $3.15 |
| [H100 PCIE](https://corehu.com/gpus/h100-pcie) | 80 GB | $4.82 |
| [H200](https://corehu.com/gpus/h200) | 141 GB | $6.15 |
| [B200](https://corehu.com/gpus/b200) | 179 GB | $12.39 |
| [RTX PRO 6000](https://corehu.com/gpus/rtx-pro-6000) | 96 GB | $4.21 |

All 92 GPU models: [`data/gpu_prices_latest.csv`](data/gpu_prices_latest.csv). Live prices: [corehu.com/gpu-prices](https://corehu.com/gpu-prices).

## Files

- `data/gpu_prices_latest.csv`: `date, gpu, slug, vram_gb, usd_per_hour_from, url`. The price is the cheapest rentable offer, per GPU; machines with several GPUs are divided by their GPU count.
- `data/gpu_price_index_daily.csv`: `day, gpu, index, offers_tracked`. For each GPU model, the median offer price relative to its first tracked day (= 100).

## Related

- [How much GPU memory does an open model need?](https://corehu.com/run): VRAM needs and live run cost for ~60,000 Hugging Face models.
- [Best GPU for 70B LLMs, FLUX, fine-tuning and more](https://corehu.com/best-gpu/llm-70b).
- [GPU comparisons](https://corehu.com/gpus/compare/rtx-4090-vs-rtx-5090).
- Also published on Hugging Face as [corehu-cloud/gpu-cloud-prices](https://huggingface.co/datasets/corehu-cloud/gpu-cloud-prices), with a [VRAM calculator Space](https://huggingface.co/spaces/corehu-cloud/vram-calculator).

## License

Data: CC BY 4.0. Please cite "CoreHu GPU price data, https://corehu.com/gpu-prices".
