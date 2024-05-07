# Getting Started with Nosana

Nosana is a DePin(Decentralized Physical Infrastructure) that uses the Solana Blockchain to provide the Open Source AI Community with full decentralized compute to run AI inference

### How To Use Nosana?
Nosana works pretty simple. We have markets that are [insert more info]. And there are jobs, docker images that you can run on our NVIDIA Nodes of your AI inference.

### How To Write A Nosana Job

This is the basic structure of a nosana job 

```
{
  "version": "0.1",
  "type": "container",
  "meta": {
    "trigger": "cli"
  },
  "ops": [
    {
      "type": "container/run",
      "id": "llama2",
      "args": {
        "cmd": ["python3 llama2.py 'What colour is the sky?'"],
        "image": "docker.io/matthammond962/llama2-python-gpu-binding",
        "gpu": true
      }
    }
  ]
}
```
