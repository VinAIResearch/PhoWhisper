# PhoWhisper:  Automatic  Speech  Recognition for  Vietnamese


We introduce **PhoWhisper** in five versions for Vietnamese automatic speech recognition. PhoWhisper's robustness is achieved through fine-tuning the multilingual [Whisper](https://github.com/openai/whisper)  on an 844-hour dataset that encompasses diverse Vietnamese accents. Our experimental study demonstrates state-of-the-art performances of PhoWhisper on benchmark Vietnamese ASR datasets. Please **cite** [our PhoWhisper paper](https://openreview.net/pdf?id=qsif2awK2L) when it is used to help produce published results or is incorporated into other software:

```
@inproceedings{PhoWhisper,
  title     = {{PhoWhisper: Automatic Speech Recognition for Vietnamese}},
  author    = {Thanh-Thien Le and Linh The Nguyen and Dat Quoc Nguyen},
  booktitle = {Proceedings of the ICLR 2024 Tiny Papers track},
  year      = {2024}
}
```

## Model download & WER results

| Model | #paras | CMV–Vi | VIVOS | VLSP 2020 Task-1 | VLSP 2020 Task-2
|---|---|---|---|---|---|
[`vinai/PhoWhisper-tiny`](https://huggingface.co/vinai/PhoWhisper-tiny) | 39M |19.05 |10.41 |20.74 |49.85
[`vinai/PhoWhisper-base`](https://huggingface.co/vinai/PhoWhisper-base) | 74M |16.19 |8.46 |19.70| 43.01
[`vinai/PhoWhisper-small`](https://huggingface.co/vinai/PhoWhisper-small) | 244M |11.08 |6.33 |15.93 |32.96
[`vinai/PhoWhisper-medium`](https://huggingface.co/vinai/PhoWhisper-medium) | 769M |8.27 |4.97 |14.12 |26.85
[`vinai/PhoWhisper-large`](https://huggingface.co/vinai/PhoWhisper-large) | **1.55B** |**8.14** |**4.67** |**13.75** |**26.68**
<!--`wav2vec2-base-vietnamese-250h` |95M |102.04 |10.83 |21.02 |50.35
`wav2vec2-base-vi-vlsp2020` |95M |103.71| 9.90 |16.82 |44.91
`wav2vec2-large-vi-vlsp2020` |317M |101.41 |8.61 |15.18 |36.75-->

## Run the model

#### Example usage with transformers

```python
from transformers import pipeline
transcriber = pipeline("automatic-speech-recognition", model="vinai/PhoWhisper-small")
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
