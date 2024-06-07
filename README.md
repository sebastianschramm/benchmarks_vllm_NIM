# Benchmarks of request throughput of vllm and NVIDIA NIM

Using [vllm benchmark script](https://github.com/vllm-project/vllm/blob/main/benchmarks/benchmark_serving.py) I evaluated
[llama-3-8B-instruct](https://huggingface.co/meta-llama/Meta-Llama-3-8B-Instruct) served with [vllm](https://github.com/vllm-project/vllm) and with [NVIDIA NIM](https://www.nvidia.com/en-us/ai/)
and deployed on AWS via HuggingFace Endpoints on two different instance types - L4 and A10G.

## Results

For the shareGPT dataset on A10G, vllm has 18% higher request throughput compare to NIM.

Average over 2 runs:

Hardware | vllm | NIM
--- | --- | ---
L4 |  2.73 | 2.61
A10G | 4.13 | 3.49

![Request throughput comparison](./request_throughput.png?raw=true)

The repo contains benchmark JSON files for more details.
