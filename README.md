# THRML-HACK

```
uv init
uv add verifiers
```

```
uv run vf-init my-env
uv pip install -e environments/my-env
```

For starters paste [reverse-text](https://github.com/PrimeIntellect-ai/verifiers/blob/main/environments/reverse_text/reverse_text.py) into your env.

Sanity check. Set `OPENAI_API_KEY` and run a small eval.
```
uv run vf-eval my-env
```


Download and install `prime-rl` trainer.
```
uv run vf-setup
```

Copy [configs/reverse_text/rl.toml](configs/reverse_text/rl.toml) to `prime-rl/configs/reverse_text/rl.toml`.
Run RL training. Login to or set you wandb api key.
```
uv run rl @ configs/reverse_text/rl.toml
```

