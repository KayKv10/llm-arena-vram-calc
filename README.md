# LLM Arena VRAM Calculator

Enriches the [Arena.ai](https://arena.ai/leaderboard/text?license=open-source) open-source LLM leaderboard with parameter counts and VRAM estimates for single-GPU deployment feasibility.

Most LLM leaderboards rank models by quality but ignore deployment constraints. This tool answers: *"What's the best model I can actually run on my hardware?"* by cross-referencing Arena rankings with VRAM requirements across precisions.

> **Last updated:** 2026-08-08 06:41 UTC | **Models:** 213 | **Resolved:** 165 (77.5%)

> **Warning:** AA data may be stale (RSC fetch failed, using cached data).

## Best Model Per GPU

Highest-ranked Arena model that fits on each single GPU (includes 25% serving overhead for KV cache, activations, and framework).

### BF16 (Full Precision)

| GPU | VRAM | Best Model | Arena Rank | Params | Arch | Serving VRAM |
|-----|------|------------|------------|--------|------|--------------|
| H100 SXM | 80 GB | gemma-4-31b | #10 | 31B | Dense | 77.5 GB |
| RTX PRO 6000 | 96 GB | gemma-4-31b | #10 | 31B | Dense | 77.5 GB |
| H200 SXM | 141 GB | gemma-4-31b | #10 | 31B | Dense | 77.5 GB |
| B200 SXM | 180 GB | gemma-4-31b | #10 | 31B | Dense | 77.5 GB |
| B300 SXM | 288 GB | gemma-4-31b | #10 | 31B | Dense | 77.5 GB |

### FP8 (8-bit)

| GPU | VRAM | Best Model | Arena Rank | Params | Arch | Serving VRAM |
|-----|------|------------|------------|--------|------|--------------|
| H100 SXM | 80 GB | gemma-4-31b | #10 | 31B | Dense | 38.8 GB |
| RTX PRO 6000 | 96 GB | gemma-4-31b | #10 | 31B | Dense | 38.8 GB |
| H200 SXM | 141 GB | gemma-4-31b | #10 | 31B | Dense | 38.8 GB |
| B200 SXM | 180 GB | gemma-4-31b | #10 | 31B | Dense | 38.8 GB |
| B300 SXM | 288 GB | gemma-4-31b | #10 | 31B | Dense | 38.8 GB |

### INT4 (4-bit)

| GPU | VRAM | Best Model | Arena Rank | Params | Arch | Serving VRAM |
|-----|------|------------|------------|--------|------|--------------|
| H100 SXM | 80 GB | gemma-4-31b | #10 | 31B | Dense | 19.4 GB |
| RTX PRO 6000 | 96 GB | gemma-4-31b | #10 | 31B | Dense | 19.4 GB |
| H200 SXM | 141 GB | gemma-4-31b | #10 | 31B | Dense | 19.4 GB |
| B200 SXM | 180 GB | gemma-4-31b | #10 | 31B | Dense | 19.4 GB |
| B300 SXM | 288 GB | hy3 | #9 | 299B | MoE | 186.9 GB |

## Full Leaderboard

| Rank | Model | Score | Params (B) | Arch | VRAM BF16 | VRAM FP8 | VRAM INT4 | Fits on |
|------|-------|-------|------------|------|-----------|----------|-----------|---------|
| 1 | kimi-k3-max | 1485 | ? | ? | ? | ? | ? | ? |
| 2 | glm-5.2-max | 1470 | ? | ? | ? | ? | ? | ? |
| 3 | glm-5.1 | 1467 | ? | ? | ? | ? | ? | ? |
| 4 | mimo-v2.5-pro | 1467 | ? | ? | ? | ? | ? | ? |
| 5 | kimi-k2.6 | 1460 | 1000 (32) | MoE | 2500 | 1250 | 625 | Multi-GPU |
| 6 | deepseek-v4-pro | 1457 | 1600 (49) | MoE | 4000 | 2000 | 1000 | Multi-GPU |
| 7 | glm-5 | 1456 | 744 (40) | MoE | 1860 | 930 | 465 | Multi-GPU |
| 8 | deepseek-v4-pro-high-preview | 1455 | ? | ? | ? | ? | ? | ? |
| 9 | hy3 | 1453 | 299 (21) | MoE | 747.5 | 373.8 | 186.9 | Multi-GPU |
| 10 | gemma-4-31b | 1450 | 31 | Dense | 77.5 | 38.8 | 19.4 | H100 SXM (FP8) |
| 11 | kimi-k2.5-thinking | 1450 | 1000 (32) | MoE | 2500 | 1250 | 625 | Multi-GPU |
| 12 | minimax-m3 | 1444 | 428 (23) | MoE | 1070 | 535 | 267.5 | Multi-GPU |
| 13 | qwen3.5-397b-a17b | 1442 | 397 (17) | MoE | 992.5 | 496.2 | 248.1 | Multi-GPU |
| 14 | glm-4.7 | 1441 | ? | ? | ? | ? | ? | ? |
| 15 | inkling | 1441 | 975 (41) | MoE | 2437.5 | 1218.8 | 609.4 | Multi-GPU |
| 16 | gemma-4-26b-a4b | 1438 | 26 (4) | MoE | 65 | 32.5 | 16.2 | H100 SXM (FP8) |
| 17 | deepseek-v4-flash-high-preview | 1437 | ? | ? | ? | ? | ? | ? |
| 18 | deepseek-v4-flash | 1435 | 284 (13) | MoE | 710 | 355 | 177.5 | Multi-GPU |
| 19 | mimo-v2.5 | 1434 | ? | ? | ? | ? | ? | ? |
| 20 | kimi-k2.5-instant | 1431 | 1000 (32) | MoE | 2500 | 1250 | 625 | Multi-GPU |
| 21 | kimi-k2-thinking-turbo | 1429 | 1000 (32) | MoE | 2500 | 1250 | 625 | Multi-GPU |
| 22 | mistral-medium-3.5 | 1427 | ? | ? | ? | ? | ? | ? |
| 23 | nvidia-nemotron-3-ultra-550b-a55b-nvfp4 | 1426 | 550 (55) | MoE | 1375 | 687.5 | 343.8 | Multi-GPU |
| 24 | deepseek-v3.2 | 1425 | ? | ? | ? | ? | ? | ? |
| 25 | glm-4.6 | 1424 | ? | ? | ? | ? | ? | ? |
| 26 | deepseek-v3.2-exp-thinking | 1424 | ? | ? | ? | ? | ? | ? |
| 27 | qwen3-235b-a22b-instruct-2507 | 1422 | 235 (22) | MoE | 587.5 | 293.8 | 146.9 | Multi-GPU |
| 28 | deepseek-v3.2-thinking | 1422 | ? | ? | ? | ? | ? | ? |
| 29 | deepseek-v3.2-exp | 1422 | ? | ? | ? | ? | ? | ? |
| 30 | deepseek-r1-0528 | 1422 | ? | ? | ? | ? | ? | ? |
| 31 | kimi-k2-0905-preview | 1418 | 1000 (32) | MoE | 2500 | 1250 | 625 | Multi-GPU |
| 32 | kimi-k2-0711-preview | 1417 | 1000 (32) | MoE | 2500 | 1250 | 625 | Multi-GPU |
| 33 | deepseek-v3.1 | 1417 | ? | ? | ? | ? | ? | ? |
| 34 | deepseek-v3.1-terminus-thinking | 1417 | ? | ? | ? | ? | ? | ? |
| 35 | qwen3.5-122b-a10b | 1416 | 122 (10) | MoE | 305 | 152.5 | 76.2 | B200 SXM (FP8) |
| 36 | deepseek-v3.1-thinking | 1416 | ? | ? | ? | ? | ? | ? |
| 37 | minimax-m2.7 | 1415 | ? | ? | ? | ? | ? | ? |
| 38 | mistral-large-3 | 1415 | 675 (41) | MoE | 1687.5 | 843.8 | 421.9 | Multi-GPU |
| 39 | qwen3-vl-235b-a22b-instruct | 1415 | 235 (22) | MoE | 587.5 | 293.8 | 146.9 | Multi-GPU |
| 40 | deepseek-v3.1-terminus | 1415 | ? | ? | ? | ? | ? | ? |
| 41 | hunyuan-hy3-preview | 1411 | ? | ? | ? | ? | ? | ? |
| 42 | glm-4.5 | 1410 | 355 (32) | MoE | 887.5 | 443.8 | 221.9 | Multi-GPU |
| 43 | qwen3.5-27b | 1407 | 27 | Dense | 67.5 | 33.8 | 16.9 | H100 SXM (FP8) |
| 44 | qwen3-235b-a22b-no-thinking | 1402 | 235 (22) | MoE | 587.5 | 293.8 | 146.9 | Multi-GPU |
| 45 | qwen3-next-80b-a3b-instruct | 1401 | 80 (3) | MoE | 200 | 100 | 50 | H200 SXM (FP8) |
| 46 | longcat-flash-chat | 1400 | 560 (27) | MoE | 1400 | 700 | 350 | Multi-GPU |
| 47 | qwen3-235b-a22b-thinking-2507 | 1398 | 235 (22) | MoE | 587.5 | 293.8 | 146.9 | Multi-GPU |
| 48 | deepseek-r1 | 1398 | 685 (37) | MoE | 1712.5 | 856.2 | 428.1 | Multi-GPU |
| 49 | deepseek-v3-0324 | 1395 | 671 (37) | MoE | 1677.5 | 838.8 | 419.4 | Multi-GPU |
| 50 | qwen3-vl-235b-a22b-thinking | 1395 | 235 (22) | MoE | 587.5 | 293.8 | 146.9 | Multi-GPU |

<details><summary>Show remaining 163 models</summary>

| Rank | Model | Score | Params (B) | Arch | VRAM BF16 | VRAM FP8 | VRAM INT4 | Fits on |
|------|-------|-------|------------|------|-----------|----------|-----------|---------|
| 51 | qwen3.5-35b-a3b | 1395 | 35 (3) | MoE | 87.5 | 43.8 | 21.9 | H100 SXM (FP8) |
| 52 | step-3.5-flash | 1394 | ? | ? | ? | ? | ? | ? |
| 53 | mimo-v2-flash (non-thinking) | 1392 | ? | ? | ? | ? | ? | ? |
| 54 | minimax-m2.5 | 1389 | ? | ? | ? | ? | ? | ? |
| 55 | qwen3-coder-480b-a35b-instruct | 1387 | 480 (35) | MoE | 1200 | 600 | 300 | Multi-GPU |
| 56 | mimo-v2-flash (thinking) | 1386 | ? | ? | ? | ? | ? | ? |
| 57 | minimax-m2.1-preview | 1384 | ? | ? | ? | ? | ? | ? |
| 58 | qwen3-30b-a3b-instruct-2507 | 1383 | 30 (3) | MoE | 75 | 37.5 | 18.8 | H100 SXM (FP8) |
| 59 | trinity-large-preview | 1378 | 70 | Dense | 175 | 87.5 | 43.8 | RTX PRO 6000 (FP8) |
| 60 | glm-4.6v | 1377 | ? | ? | ? | ? | ? | ? |
| 61 | qwen3-235b-a22b | 1374 | 235 (22) | MoE | 587.5 | 293.8 | 146.9 | Multi-GPU |
| 62 | glm-4.5-air | 1372 | ? | ? | ? | ? | ? | ? |
| 63 | qwen3-next-80b-a3b-thinking | 1369 | 80 (3) | MoE | 200 | 100 | 50 | H200 SXM (FP8) |
| 64 | trinity-large-thinking | 1368 | 70 | Dense | 175 | 87.5 | 43.8 | RTX PRO 6000 (FP8) |
| 65 | glm-4.7-flash | 1367 | ? | ? | ? | ? | ? | ? |
| 66 | gemma-3-27b-it | 1365 | 27 | Dense | 67.5 | 33.8 | 16.9 | H100 SXM (FP8) |
| 67 | minimax-m1 | 1363 | ? | ? | ? | ? | ? | ? |
| 68 | nvidia-nemotron-3-super-120b-a12b | 1360 | 120 (12) | MoE | 300 | 150 | 75 | B200 SXM (FP8) |
| 69 | deepseek-v3 | 1358 | 671 (37) | MoE | 1677.5 | 838.8 | 419.4 | Multi-GPU |
| 70 | mistral-small-2506 | 1357 | ? | ? | ? | ? | ? | ? |
| 71 | intellect-3 | 1356 | 107 (12) | MoE | 267.5 | 133.8 | 66.9 | H200 SXM (FP8) |
| 72 | command-a-03-2025 | 1353 | ? | ? | ? | ? | ? | ? |
| 73 | glm-4.5v | 1353 | ? | ? | ? | ? | ? | ? |
| 74 | gpt-oss-120b | 1352 | 117 (5.1) | MoE | 292.5 | 146.2 | 73.1 | B200 SXM (FP8) |
| 75 | step-3 | 1348 | ? | ? | ? | ? | ? | ? |
| 76 | llama-3.1-nemotron-ultra-253b-v1 | 1347 | 253 | Dense | 632.5 | 316.2 | 158.1 | Multi-GPU |
| 77 | qwen3-32b | 1347 | 32 | Dense | 80 | 40 | 20 | H100 SXM (FP8) |
| 78 | ling-flash-2.0 | 1346 | ? | ? | ? | ? | ? | ? |
| 79 | minimax-m2 | 1346 | 230 (10) | MoE | 575 | 287.5 | 143.8 | B300 SXM (FP8) |
| 80 | nvidia-llama-3.3-nemotron-super-49b-v1.5 | 1343 | 49 | Dense | 122.5 | 61.2 | 30.6 | H100 SXM (FP8) |
| 81 | gemma-3-12b-it | 1341 | 12 | Dense | 30 | 15 | 7.5 | H100 SXM (FP8) |
| 82 | qwq-32b | 1336 | 32 | Dense | 80 | 40 | 20 | H100 SXM (FP8) |
| 83 | llama-3.1-405b-instruct-bf16 | 1335 | 405 | Dense | 1012.5 | 506.2 | 253.1 | Multi-GPU |
| 84 | llama-3.1-405b-instruct-fp8 | 1333 | 405 | Dense | 1012.5 | 506.2 | 253.1 | Multi-GPU |
| 85 | olmo-3.1-32b-instruct | 1329 | 32 | Dense | 80 | 40 | 20 | H100 SXM (FP8) |
| 86 | molmo-2-8b | 1328 | 8 | Dense | 20 | 10 | 5 | H100 SXM (FP8) |
| 87 | llama-3.3-nemotron-49b-super-v1 | 1328 | 49 | Dense | 122.5 | 61.2 | 30.6 | H100 SXM (FP8) |
| 88 | qwen3-30b-a3b | 1327 | 30 (3) | MoE | 75 | 37.5 | 18.8 | H100 SXM (FP8) |
| 89 | llama-4-maverick-17b-128e-instruct | 1327 | 400 (17) | MoE | 1000 | 500 | 250 | Multi-GPU |
| 90 | deepseek-v2.5-1210 | 1323 | ? | ? | ? | ? | ? | ? |
| 91 | llama-4-scout-17b-16e-instruct | 1322 | 109 (17) | MoE | 272.5 | 136.2 | 68.1 | H200 SXM (FP8) |
| 92 | ring-flash-2.0 | 1320 | ? | ? | ? | ? | ? | ? |
| 93 | llama-3.3-70b-instruct | 1318 | 70 | Dense | 175 | 87.5 | 43.8 | RTX PRO 6000 (FP8) |
| 94 | gemma-3n-e4b-it | 1318 | 8.4 (4) | MoE | 21 | 10.5 | 5.2 | H100 SXM (FP8) |
| 95 | qwen-max-0919 | 1318 | ? | ? | ? | ? | ? | ? |
| 96 | gpt-oss-20b | 1317 | 21 (3.6) | MoE | 52.5 | 26.2 | 13.1 | H100 SXM (FP8) |
| 97 | nvidia-nemotron-3-nano-30b-a3b-bf16 | 1315 | 30 (3) | MoE | 75 | 37.5 | 18.8 | H100 SXM (FP8) |
| 98 | athene-v2-chat | 1314 | 72 | Dense | 180 | 90 | 45 | RTX PRO 6000 (FP8) |
| 99 | mistral-large-2407 | 1314 | 123 | Dense | 307.5 | 153.8 | 76.9 | B200 SXM (FP8) |
| 100 | deepseek-v2.5 | 1307 | ? | ? | ? | ? | ? | ? |
| 101 | athene-70b-0725 | 1306 | 70 | Dense | 175 | 87.5 | 43.8 | RTX PRO 6000 (FP8) |
| 102 | granite-4.1-8b | 1305 | 8 | Dense | 20 | 10 | 5 | H100 SXM (FP8) |
| 103 | olmo-3-32b-think | 1305 | 32 | Dense | 80 | 40 | 20 | H100 SXM (FP8) |
| 104 | mistral-large-2411 | 1305 | ? | ? | ? | ? | ? | ? |
| 105 | gemma-3-4b-it | 1303 | 4 | Dense | 10 | 5 | 2.5 | H100 SXM (FP8) |
| 106 | mistral-small-3.1-24b-instruct-2503 | 1303 | 24 | Dense | 60 | 30 | 15 | H100 SXM (FP8) |
| 107 | qwen2.5-72b-instruct | 1302 | 72 | Dense | 180 | 90 | 45 | RTX PRO 6000 (FP8) |
| 108 | llama-3.1-nemotron-70b-instruct | 1299 | 70 | Dense | 175 | 87.5 | 43.8 | RTX PRO 6000 (FP8) |
| 109 | llama-3.1-70b-instruct | 1293 | 70 | Dense | 175 | 87.5 | 43.8 | RTX PRO 6000 (FP8) |
| 110 | jamba-1.5-large | 1289 | ? | ? | ? | ? | ? | ? |
| 111 | gemma-2-27b-it | 1289 | 27 | Dense | 67.5 | 33.8 | 16.9 | H100 SXM (FP8) |
| 112 | ibm-granite-h-small | 1287 | 8 | Dense | 20 | 10 | 5 | H100 SXM (FP8) |
| 113 | llama-3.1-nemotron-51b-instruct | 1286 | 51 | Dense | 127.5 | 63.8 | 31.9 | H100 SXM (FP8) |
| 114 | llama-3.1-tulu-3-70b | 1286 | 70 | Dense | 175 | 87.5 | 43.8 | RTX PRO 6000 (FP8) |
| 115 | olmo-3.1-32b-think | 1285 | 32 | Dense | 80 | 40 | 20 | H100 SXM (FP8) |
| 116 | gemma-2-9b-it-simpo | 1280 | 9 | Dense | 22.5 | 11.2 | 5.6 | H100 SXM (FP8) |
| 117 | nemotron-4-340b-instruct | 1276 | 340 | Dense | 850 | 425 | 212.5 | Multi-GPU |
| 118 | llama-3-70b-instruct | 1276 | 70 | Dense | 175 | 87.5 | 43.8 | RTX PRO 6000 (FP8) |
| 119 | command-r-plus-08-2024 | 1275 | 104 | Dense | 260 | 130 | 65 | H200 SXM (FP8) |
| 120 | mistral-small-24b-instruct-2501 | 1274 | 24 | Dense | 60 | 30 | 15 | H100 SXM (FP8) |
| 121 | qwen2.5-coder-32b-instruct | 1270 | 32 | Dense | 80 | 40 | 20 | H100 SXM (FP8) |
| 122 | c4ai-aya-expanse-32b | 1267 | 32 | Dense | 80 | 40 | 20 | H100 SXM (FP8) |
| 123 | gemma-2-9b-it | 1266 | 9 | Dense | 22.5 | 11.2 | 5.6 | H100 SXM (FP8) |
| 124 | deepseek-coder-v2 | 1264 | 236 (21) | MoE | 590 | 295 | 147.5 | Multi-GPU |
| 125 | qwen2-72b-instruct | 1261 | 72 | Dense | 180 | 90 | 45 | RTX PRO 6000 (FP8) |
| 126 | command-r-plus | 1261 | ? | ? | ? | ? | ? | ? |
| 127 | phi-4 | 1256 | 14 | Dense | 35 | 17.5 | 8.8 | H100 SXM (FP8) |
| 128 | olmo-2-0325-32b-instruct | 1251 | 32 | Dense | 80 | 40 | 20 | H100 SXM (FP8) |
| 129 | command-r-08-2024 | 1249 | 35 | Dense | 87.5 | 43.8 | 21.9 | H100 SXM (FP8) |
| 130 | jamba-1.5-mini | 1239 | ? | ? | ? | ? | ? | ? |
| 131 | ministral-8b-2410 | 1237 | 8 | Dense | 20 | 10 | 5 | H100 SXM (FP8) |
| 132 | qwen1.5-110b-chat | 1233 | 110 | Dense | 275 | 137.5 | 68.8 | H200 SXM (FP8) |
| 133 | qwen1.5-72b-chat | 1232 | 72 | Dense | 180 | 90 | 45 | RTX PRO 6000 (FP8) |
| 134 | mixtral-8x22b-instruct-v0.1 | 1228 | 140.8 (39.6) | MoE | 352 | 176 | 88 | B200 SXM (FP8) |
| 135 | command-r | 1226 | ? | ? | ? | ? | ? | ? |
| 136 | llama-3-8b-instruct | 1223 | 8 | Dense | 20 | 10 | 5 | H100 SXM (FP8) |
| 137 | c4ai-aya-expanse-8b | 1222 | 8 | Dense | 20 | 10 | 5 | H100 SXM (FP8) |
| 138 | llama-3.1-tulu-3-8b | 1220 | 8 | Dense | 20 | 10 | 5 | H100 SXM (FP8) |
| 139 | yi-1.5-34b-chat | 1212 | 34 | Dense | 85 | 42.5 | 21.2 | H100 SXM (FP8) |
| 140 | zephyr-orpo-141b-A35b-v0.1 | 1212 | 141 (35) | MoE | 352.5 | 176.2 | 88.1 | B200 SXM (FP8) |
| 141 | llama-3.1-8b-instruct | 1211 | 8 | Dense | 20 | 10 | 5 | H100 SXM (FP8) |
| 142 | granite-3.1-8b-instruct | 1208 | 8 | Dense | 20 | 10 | 5 | H100 SXM (FP8) |
| 143 | qwen1.5-32b-chat | 1203 | 32 | Dense | 80 | 40 | 20 | H100 SXM (FP8) |
| 144 | gemma-2-2b-it | 1200 | 2 | Dense | 5 | 2.5 | 1.2 | H100 SXM (FP8) |
| 145 | phi-3-medium-4k-instruct | 1197 | 14 | Dense | 35 | 17.5 | 8.8 | H100 SXM (FP8) |
| 146 | mixtral-8x7b-instruct-v0.1 | 1196 | 44.8 (12.6) | MoE | 112 | 56 | 28 | H100 SXM (FP8) |
| 147 | dbrx-instruct-preview | 1194 | ? | ? | ? | ? | ? | ? |
| 148 | internlm2_5-20b-chat | 1190 | 20 | Dense | 50 | 25 | 12.5 | H100 SXM (FP8) |
| 149 | qwen1.5-14b-chat | 1190 | 14 | Dense | 35 | 17.5 | 8.8 | H100 SXM (FP8) |
| 150 | deepseek-llm-67b-chat | 1184 | 67 | Dense | 167.5 | 83.8 | 41.9 | RTX PRO 6000 (FP8) |
| 151 | wizardlm-70b | 1184 | 70 | Dense | 175 | 87.5 | 43.8 | RTX PRO 6000 (FP8) |
| 152 | yi-34b-chat | 1183 | 34 | Dense | 85 | 42.5 | 21.2 | H100 SXM (FP8) |
| 153 | granite-3.0-8b-instruct | 1182 | 8 | Dense | 20 | 10 | 5 | H100 SXM (FP8) |
| 154 | openchat-3.5 | 1182 | ? | ? | ? | ? | ? | ? |
| 155 | openchat-3.5-0106 | 1182 | ? | ? | ? | ? | ? | ? |
| 156 | gemma-1.1-7b-it | 1181 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 157 | snowflake-arctic-instruct | 1179 | ? | ? | ? | ? | ? | ? |
| 158 | granite-3.1-2b-instruct | 1178 | 2 | Dense | 5 | 2.5 | 1.2 | H100 SXM (FP8) |
| 159 | tulu-2-dpo-70b | 1177 | 70 | Dense | 175 | 87.5 | 43.8 | RTX PRO 6000 (FP8) |
| 160 | openhermes-2.5-mistral-7b | 1175 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 161 | vicuna-33b | 1172 | 33 | Dense | 82.5 | 41.2 | 20.6 | H100 SXM (FP8) |
| 162 | starling-lm-7b-beta | 1170 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 163 | phi-3-small-8k-instruct | 1170 | 7.4 | Dense | 18.5 | 9.2 | 4.6 | H100 SXM (FP8) |
| 164 | llama-2-70b-chat | 1170 | 70 | Dense | 175 | 87.5 | 43.8 | RTX PRO 6000 (FP8) |
| 165 | starling-lm-7b-alpha | 1166 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 166 | llama-3.2-3b-instruct | 1166 | 3 | Dense | 7.5 | 3.8 | 1.9 | H100 SXM (FP8) |
| 167 | nous-hermes-2-mixtral-8x7b-dpo | 1163 | 44.8 (12.6) | MoE | 112 | 56 | 28 | H100 SXM (FP8) |
| 168 | granite-3.0-2b-instruct | 1155 | 2 | Dense | 5 | 2.5 | 1.2 | H100 SXM (FP8) |
| 169 | qwq-32b-preview | 1154 | 32 | Dense | 80 | 40 | 20 | H100 SXM (FP8) |
| 170 | llama2-70b-steerlm-chat | 1154 | 70 | Dense | 175 | 87.5 | 43.8 | RTX PRO 6000 (FP8) |
| 171 | solar-10.7b-instruct-v1.0 | 1151 | 10.7 | Dense | 26.8 | 13.4 | 6.7 | H100 SXM (FP8) |
| 172 | dolphin-2.2.1-mistral-7b | 1151 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 173 | mpt-30b-chat | 1149 | 30 | Dense | 75 | 37.5 | 18.8 | H100 SXM (FP8) |
| 174 | wizardlm-13b | 1148 | 13 | Dense | 32.5 | 16.2 | 8.1 | H100 SXM (FP8) |
| 175 | mistral-7b-instruct-v0.2 | 1148 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 176 | falcon-180b-chat | 1147 | 180 | Dense | 450 | 225 | 112.5 | B300 SXM (FP8) |
| 177 | qwen1.5-7b-chat | 1143 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 178 | phi-3-mini-4k-instruct-june-2024 | 1142 | 3.8 | Dense | 9.5 | 4.8 | 2.4 | H100 SXM (FP8) |
| 179 | llama-2-13b-chat | 1140 | 13 | Dense | 32.5 | 16.2 | 8.1 | H100 SXM (FP8) |
| 180 | vicuna-13b | 1140 | 13 | Dense | 32.5 | 16.2 | 8.1 | H100 SXM (FP8) |
| 181 | qwen-14b-chat | 1138 | 14 | Dense | 35 | 17.5 | 8.8 | H100 SXM (FP8) |
| 182 | gemma-7b-it | 1137 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 183 | codellama-34b-instruct | 1136 | 34 | Dense | 85 | 42.5 | 21.2 | H100 SXM (FP8) |
| 184 | zephyr-7b-beta | 1130 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 185 | phi-3-mini-128k-instruct | 1129 | 3.8 | Dense | 9.5 | 4.8 | 2.4 | H100 SXM (FP8) |
| 186 | phi-3-mini-4k-instruct | 1127 | 3.8 | Dense | 9.5 | 4.8 | 2.4 | H100 SXM (FP8) |
| 187 | guanaco-33b | 1126 | 33 | Dense | 82.5 | 41.2 | 20.6 | H100 SXM (FP8) |
| 188 | zephyr-7b-alpha | 1126 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 189 | stripedhyena-nous-7b | 1120 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 190 | codellama-70b-instruct | 1118 | 70 | Dense | 175 | 87.5 | 43.8 | RTX PRO 6000 (FP8) |
| 191 | gemma-1.1-2b-it | 1115 | 2 | Dense | 5 | 2.5 | 1.2 | H100 SXM (FP8) |
| 192 | vicuna-7b | 1114 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 193 | smollm2-1.7b-instruct | 1114 | 1.7 | Dense | 4.2 | 2.1 | 1.1 | H100 SXM (FP8) |
| 194 | llama-3.2-1b-instruct | 1110 | 1 | Dense | 2.5 | 1.2 | 0.6 | H100 SXM (FP8) |
| 195 | mistral-7b-instruct | 1109 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 196 | llama-2-7b-chat | 1107 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 197 | gemma-2b-it | 1092 | 2 | Dense | 5 | 2.5 | 1.2 | H100 SXM (FP8) |
| 198 | qwen1.5-4b-chat | 1090 | 4 | Dense | 10 | 5 | 2.5 | H100 SXM (FP8) |
| 199 | olmo-7b-instruct | 1073 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 200 | koala-13b | 1070 | 13 | Dense | 32.5 | 16.2 | 8.1 | H100 SXM (FP8) |
| 201 | alpaca-13b | 1068 | 13 | Dense | 32.5 | 16.2 | 8.1 | H100 SXM (FP8) |
| 202 | gpt4all-13b-snoozy | 1066 | 13 | Dense | 32.5 | 16.2 | 8.1 | H100 SXM (FP8) |
| 203 | mpt-7b-chat | 1062 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 204 | chatglm3-6b | 1055 | 6 | Dense | 15 | 7.5 | 3.8 | H100 SXM (FP8) |
| 205 | RWKV-4-Raven-14B | 1041 | 14 | Dense | 35 | 17.5 | 8.8 | H100 SXM (FP8) |
| 206 | chatglm2-6b | 1023 | 6 | Dense | 15 | 7.5 | 3.8 | H100 SXM (FP8) |
| 207 | oasst-pythia-12b | 1022 | 12 | Dense | 30 | 15 | 7.5 | H100 SXM (FP8) |
| 208 | chatglm-6b | 995 | 6 | Dense | 15 | 7.5 | 3.8 | H100 SXM (FP8) |
| 209 | fastchat-t5-3b | 991 | 3 | Dense | 7.5 | 3.8 | 1.9 | H100 SXM (FP8) |
| 210 | dolly-v2-12b | 981 | 12 | Dense | 30 | 15 | 7.5 | H100 SXM (FP8) |
| 211 | llama-13b | 973 | 13 | Dense | 32.5 | 16.2 | 8.1 | H100 SXM (FP8) |
| 212 | stablelm-tuned-alpha-7b | 952 | 7 | Dense | 17.5 | 8.8 | 4.4 | H100 SXM (FP8) |
| 213 | inkling-small | 1430 | 266 (12) | MoE | 665 | 332.5 | 166.2 | Multi-GPU |

</details>

## Architecture

**Data flow:** Arena.ai leaderboard → parameter resolution (4-strategy fallback) → VRAM calculation → GPU feasibility matrix

The parameter resolution chain prioritizes accuracy: manual overrides catch known errors, [Artificial Analysis](https://artificialanalysis.ai) provides bulk data for 400+ models via a single RSC stream request (cached locally, 24h TTL), name parsing extracts `{N}B` patterns as a fallback, and per-model page scraping handles the long tail.

### VRAM Estimation

| Precision | Bytes/Param | Example: 70B model |
|-----------|-------------|---------------------|
| BF16 | 2.0 | 140 GB weights, 175 GB serving |
| FP8 | 1.0 | 70 GB weights, 87.5 GB serving |
| INT4 | 0.5 | 35 GB weights, 43.8 GB serving |

**Serving VRAM** = weight VRAM × 1.25 (25% overhead for KV cache, activations, framework). For **MoE models**, all experts must be loaded regardless of active count.

### GPUs

| GPU | VRAM | Architecture | Native FP8 |
|-----|------|-------------|------------|
| H100 SXM | 80 GB | Hopper | Yes |
| RTX PRO 6000 | 96 GB | Ada Lovelace | No (software emulation) |
| H200 SXM | 141 GB | Hopper | Yes |
| B200 SXM | 180 GB | Blackwell | Yes |
| B300 SXM | 288 GB | Blackwell Ultra | Yes |

## Usage

```bash
# Install dependencies
uv sync

# Full pipeline (scrapes arena.ai live, updates README)
uv run python arena_enrichment/enrich_arena.py --update-readme

# Use a pre-downloaded CSV
uv run python arena_enrichment/enrich_arena.py --input data.csv --update-readme

# Skip network resolution (overrides + name parsing only)
uv run python arena_enrichment/enrich_arena.py --no-network --update-readme
```
