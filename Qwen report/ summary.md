QWEN research:
The general models:
-Qwen 1 (Aug-Dec 2023):Chinese+English only, 1.8B, 7B, 14B, and 72B, context window=32K tokens, similar to LLaMA in architecture, 3 trillion tokens training.
-Qwen 1.5 (Feb 2024): More size (0.5B to 110B), MoE model, Apache 2.0, context window=32k tokens
-Qwen 2 (Jun 2024): context window=128k tokens, trained on 7 trillion tokens, 29 lannguages, proper MoE varient(57B total with 14B active at once), better coding.
-Qwen 2.5 (Sep 2024): trained on 18 trillion tokens, conext window=1million tokens, Turbo varient, 29 languages, specialized sub models where released (coding, mathm vision).
-Qwen 3 (Apr 2025): trained on 36 trillion tokens, 119 languages, dual mode system (fast casual response OR deep step by step reasoning), MoE flagship with 235B total (22B at a time) 
-Qwen 3.5/3.6 (2025- Apr 2026):  new hybrid architecture, can run on a 24GB GPU
the specialized branches:
- Qwen-VL: sees images and video
- Qwen-Audio/ Omni: hears audio, speaks back 
- Qwen-Coder: code generation
- Qwen-Math: can do math and call python interpreter mid reasoning
- QwQ: pure reasoning model, similar to OpenAI's o1, extended chain of thought
Note: Moe is Mixture of Experts.


Architecture
- SwiGLU actiovation function (smoother than ReLU)
- RoPE positional embedding (better for longer sequences)
- RMSNorm instead of LayerNorm  (faster, more stable)
- MoE added starting from Qwen 1.5
- Daul Chunk Attention (DCA) + YaRN  + DPO introduced in Qwen 2 
- Qwen VL: added a vision encoder, a model that takes in iamges turns them into tokens.
- Qwen2 VL: Naive Dynamic resolution (process images at their native resolution), video understanding.
- Qwen3 VL: thinking but with images (diagrams, complex charts,etc...)
- Qwen Audio (1,2,2.4 Omni): speach transiption (Whisper-style), multiple language, multiple speakers, non speach sounds (Barking for example)
NOTE:Omni means it has all the other speciaties (Text, Image, Video, Audio, Speach)
Benchmarks:
- General Knowlege/Reasoning: MMLU, MMLU-Pro, GPQA
- Coding: HumanEval, LiveCodeBench,  Codeforces rating
- Math: GSM8K, MATH, AIME 24/25
- Instruction following: IFEval, ArenaHard
