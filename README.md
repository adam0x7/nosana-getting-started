# Getting Started with Nosana

Nosana is a DePin(Decentralized Physical Infrastructure) that uses the Solana Blockchain to provide the Open Source AI Community with full decentralized compute to run AI inference

### How To Use Nosana?
Nosana works pretty simple. We have markets that are [insert more info]. And there are jobs, docker images that you can run on our NVIDIA Nodes of your AI inference.

- Below, you can write the following commands in terminal to get started running AI inference on our network. 
- Git clone this repository
- And run the command below in terminal(make sure that you're still in the repository folder)
```
nosana job post --file image_gen_jobs/image_gen_1.json --market RXP7JK8MTY4uPJng4UjC9ZJdDDSG6wGr8pvVf3mwgXF --wait
```

We also have several other types of jobs with different models that you can use to run common inference. Just replace the value of the ``file`` to the desired folder/file 
### How To Write A Nosana Job

This is the basic structure of a nosana job (todo: explain parameters)

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
If you don't have the equipment to build docker images that you can run your own job on, Nosana has already given some pre built images for you to use below

### Running Jobs Locally
* Please note that there is a hardware requirement for this section
* 