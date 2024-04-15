# AnimateDiff's Prompt Travel with Regional Prompter Sample (need to enable dynamic prompts)

## My Testing Environment
* OS: Linux 6.6.25-1-MANJARO
* GPU: NVIDIA GeForce RTX 3060 VRAM 12G
* CUDA Version: 12.3.107
* Python Version: 3.11.8
* PyTorch Version: 2.2.1+cu121
* Gradio Version: 3.41.2
* Webui-forge Version: f0.0.17v1.8.0rc-latest-276-g29be1da7 
* Regional Prompter Version: 50493ec0
* AnimateDiff(sd-forge-animatediff) Version: b20f7519
* Dynamic Prompts Version: 

## Animated Samples (24frame,8fps)

### with Regional Prompter
#### Samples
* ![Sample01](SampleAnimations/00016-3418874118.webp)
* ![Sample02](SampleAnimations/00152-752436473.webp)
* ![Sample03](SampleAnimations/00218-1320549600.webp)
#### Prompt
* https://raw.githubusercontent.com/SuperHimoYarouWorld/UseAnimateDiffPromptTravelwithRegionalPrompterSample/main/SampleAnimations/00016-3418874118.txt
* https://raw.githubusercontent.com/SuperHimoYarouWorld/UseAnimateDiffPromptTravelwithRegionalPrompterSample/main/SampleAnimations/00152-752436473.txt
* https://raw.githubusercontent.com/SuperHimoYarouWorld/UseAnimateDiffPromptTravelwithRegionalPrompterSample/main/SampleAnimations/00218-1320549600.txt
#### My Regional Prompter Settings
* Active = True
* Generation Mode = Attention,Matrix
* Base Ratio = 0
* usebase = False
* usecom = False
* usencom = False
* Main Splitting = Columns
* Divide Ratio = 1,1
* Width = 1024 #for the image size is 1024x576
* Height = 576 #for the image size is 1024x576
* flip","and";" = False
* Overlay Ratio = 0.8
* Presets: None
* LoRA stop step = 0
* LoRA Hires stop step = 0
* LoRA in negative textencoder = 0
* LoRA in negative U-net = 0
* disable convert 'AND' to 'BREAK' = False
* Use LoHa or other = False
* Use BREAK to change chunks = False
* debug = False
* debug2 = True

## How to do that?

### with Stable Diffusion Web UI
Install and enable these extensions below. Then, write your prompts like Samples.
* AnimateDiff extension
* * https://github.com/continue-revolution/sd-webui-animatediff
* Dynamic Prompts extension
* * https://github.com/adieyal/sd-dynamic-prompts
* Regional Prompter extension
* * https://github.com/hako-mikan/sd-webui-regional-prompter
### with Stable Diffusion Web UI forge
Install and enable these extensions below. Then, write your prompts like Samples.
* AnimateDiff extension (for forge)
* * https://github.com/continue-revolution/sd-forge-animatediff
* Dynamic Prompts extension
* * https://github.com/adieyal/sd-dynamic-prompts
* Regional Prompter extension
* * https://github.com/hako-mikan/sd-webui-regional-prompter
