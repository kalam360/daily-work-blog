# Todo
## Reinforcement Learning in Trading
Target is to create a library with pytorch for RL in various trading environment and agents such as crypto, market-making, stocks, options, forex
- [ ] Git Repo Reproduce
    - [ ] [Gym-Anytrading](https://github.com/AminHP/gym-anytrading)
    - [ ] [gym-mtsim](https://github.com/AminHP/gym-mtsim)
    - [ ] [DI engine](https://github.com/opendilab/DI-engine)
    - [ ] [TensorTrade](https://github.com/tensortrade-org/tensortrade)
    - [ ] [Crypto-RL](https://github.com/sadighian/crypto-rl)
## Reinforcement Learning in Economic Simulation
The reinforment learning enviromnet for economic agents for various policy research. Mostly focused on macroeconomic simulation such as interest rate, monetary policy, budget policy, Forex reserve. 


## Visualization
- [ ] Libraries
    - [ ] Output tearsheet with [Quantstats](https://github.com/ranaroussi/quantstats)

## Language model with human feedback
- [ ] Git Repo Reproduce
    - [ ] [RLHF](https://github.com/CarperAI/trlx)
    - [ ] [blog post to go through](https://huggingface.co/blog/how-to-train)
    - [ ] [blog on instrucgpt](https://openai.com/blog/instruction-following/)
    - [ ] [rlhf huggingface blog](https://huggingface.co/blog/rlhf)
    - [ ] [RL4LMs](https://github.com/allenai/RL4LMs)
    - [ ] [Datasets](https://huggingface.co/datasets/Anthropic/hh-rlhf)
## Build gym environment for trading
- [ ] Liquidity Mining Env
- [ ] Stocks Env
- [ ] Options Env
- [ ] Market Making Env
- [ ] Crypto Env
- [ ] Defi Env

## Build RL-Agents for trading
- [ ] DQN Agents
- [ ] DDQN Agents

TODO: How to use Human feedback in trading environment

## Trukkr Credit Rating
- [ ] Clean and create data pipeline for soucing credit data
- [ ] Extract features from the data
- [ ] Redo the credit model

## [Stable Baselines 3](https://github.com/DLR-RM/stable-baselines3)
It  is a set of reliable implementations of reinforcement learning algorithms in PyTorch. [Docs](https://stable-baselines3.readthedocs.io/en/master/index.html) can be found here.

## [ABIDES](https://github.com/jpmorganchase/abides-jpmc-public)


## [AI-Economist](https://github.com/salesforce/ai-economist)
Gym like environment for economic simulations
### Activation key problem [Analysing RSA]
RSA key generation algorithm involves, getting two large prime numbers $p$ and $q$ such that $N = p*q$ is the public key. Now, take $e$ as a known parameter. The private key $d$ becomes:
$$ d * e = 1 \space (mod[p-1]*[q-1]) $$

Now the encryption function:
$$ c = M^e (mod N) $$

and decryption function:
$$ M = c^d (mod N) $$

There are several elements to explain but the most important is to understand why this function, which is used for decrypting $(c)$ and obtaining $[M]$, works:

$$M ≡ c^{[d]} (mod N)$$ 

This is Step 2; that is, the decryption function. I have just inverted the notation by putting $[M]$ on the left.

The reason it works is hidden in the key generation equation:
$$ [d] * e ≡ 1 \space (mod [p-1]*[q-1]) $$
$[d]$ is Alice's private key. For Euler's theorem, the function will probably be verified because the numbers $[p]$ and $[q]$ are very big and $[M]$ is probably a co-prime of $(N)$. If this equation is verified, then we can rewrite the encryption stage as follows:
$$ (M^e)^d (mod N) $$
For the properties of the powers and Euler's theorem, we have the following:
$$ M^{(e*d)} (mod N)$$
$$de ≡ 1 (mod (p-1)*(q-1))$$
That is the same as writing $M^1 = M (mod N).$ So, by inserting $[d]$ inside the decryption stage, Alice can obtain $[M]$.

### AI economist theory

### [RICE-N model for climate modeling](https://github.com/mila-iqia/climate-cooperation-competition)



## [Warpdrive package for GPU parallel processing](https://github.com/salesforce/warp-drive) 
For this to work we need [PyCUDA](https://github.com/inducer/pycuda) for that CUDA toolkit needs to install where cuda.h header file is necessary

### Multiple CUDA and cuDnn version install in ubuntu
[follow the instruction here](https://towardsdatascience.com/installing-multiple-cuda-cudnn-versions-in-ubuntu-fcb6aa5194e2)


## Utilities

- [ ] Remove pip packages from a conda environment before removing the environment
```
conda list | awk '/pypi/ {print $1}' | xargs pip uninstall -y
```
