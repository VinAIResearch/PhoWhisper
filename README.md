# PhoWhisper:  Automatic  Speech  Recognition for  Vietnamese


We introduce **PhoWhisper** in five versions for Vietnamese automatic speech recognition. PhoWhisper's robustness is achieved through fine-tuning the multilingual [Whisper](https://github.com/openai/whisper)  on an 844-hour dataset that encompasses diverse Vietnamese accents. Our experimental study demonstrates state-of-the-art performances of PhoWhisper on benchmark Vietnamese ASR datasets. Please **cite** our PhoWhisper paper when it is used to help produce published results or is incorporated into other software:

```
@inproceedings{PhoWhisper,
  title     = {{PhoWhisper: Automatic Speech Recognition for Vietnamese}},
  author    = {Thanh-Thien Le and Linh The Nguyen and Dat Quoc Nguyen},
  booktitle = {Proceedings of the ICLR 2024 Tiny Papers track},
  year      = {2024}
}
```

## Model download

| Model | #parameters |
|---|---|
[vinai/PhoWhisper-tiny](https://huggingface.co/vinai/PhoWhisper-tiny) | 39M
[vinai/PhoWhisper-base](https://huggingface.co/vinai/PhoWhisper-base) | 74M
[vinai/PhoWhisper-small](https://huggingface.co/vinai/PhoWhisper-small) | 244M
[vinai/PhoWhisper-medium](https://huggingface.co/vinai/PhoWhisper-medium) | 769M
[vinai/PhoWhisper-large](https://huggingface.co/vinai/PhoWhisper-large) | 1.55B

The following table shows word error rates on benchmarks' test sets:

<img width="500" alt="Screenshot 2024-02-21 at 11 21 22 pm" src="https://github.com/VinAIResearch/PhoWhisper/assets/2412555/370bdfa6-575e-488d-af10-7fcc2c2989f9">

## Run the model

#### Example usage with transformers

```python
from transformers import pipeline
transcriber = pipeline("automatic-speech-recognition", model="vinai/phowhisper-large")
output = transcriber(path_to_audio_with_sampling_rate_16kHz)['text']
```



## License

```
Copyright (c) 2024 VinAI Research

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
