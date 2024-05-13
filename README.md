# Apple Silicon Fix for RVC-WebUI
This repo is a dirty (and I mean really dirty) quick fix for running RVC on Apple Silicon's GPU.

+ Removes all CUDA-related code.
+ Removes all distributed logic (except for the provided distributed Sampler which can handle single device with correct arguments passed).
+ Passes all tensors to `mps` device during training.
+ Does **NOT** check if you have an `mps` device. 
+ **No** error handling, compatibility check, failure recovery, etc.. whatsoever.
+ **DO NOT USE THIS REPO UNLESS YOU'RE RUNNING IT ON APPLE SILICON**.

## Test Gig
Tested on MacBook Pro M3Max running MacOsX Sonoma 14.4

## Contributing
Contributing is what makes open source great! However please **don't** contribute to this repo as it won't be maintained or even monitored. 

Best contribution would be adapting this fix with proper checks and error handling as a PR in the awesome original repo.

[Visit the original repo](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI)

## License
[MIT](./LICENSE)