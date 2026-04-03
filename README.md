
This is an attempt to get [lemonade](https://lemonade-server.ai/) working on my own PC. 

I used vulkan (and/or rocm) here as that's what they seemed to be recommending at the time, though I did set up ROCm on my machine.

CPU: AMD Ryzen 7 5700X (8C16T)
GPU: AMD Radeon RX 6750XT (12GB VRAM) 
RAM: 32GB DDR4

To pull models exec into the lemonade server ie. `docker exec -it lemonade-server /bin/bash` and run `./lemonade-server pull <model>`. To clear all models `docker volume rm` the `cache` volume.

outcome was that the llama based models ie. `Qwen3.5-4B-GGUF` worked fine most of the time, but stable diffusion only worked on the cpu as it whinged about driver incompability with rocm or vulkan. 

