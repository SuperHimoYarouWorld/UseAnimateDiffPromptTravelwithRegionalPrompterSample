# Reagional Prompter と AnimateDiff の Prompt Travel を一緒に使ってみるテスト
* ![Regional Prompter, Different prompts can be specified for different regions](https://github.com/hako-mikan/sd-webui-regional-prompter)
* ![AnimateDiff for Stable Diffusion WebUI, You can generate GIFs in exactly the same way as generating images after enabling this extension.](https://github.com/continue-revolution/sd-webui-animatediff)

2024/04/15 時点では AnimateDiff の Prompt Travel と Regional Prompter の併用時、Dynamic Prompts 機能拡張を入れて有効にしておかないと Regional Prompter がエラーを吐きます。

## 長すぎます、読みたくありません（TL;DR）
知らんがな (´・ω・`)

## 俺氏のテスト環境
* 実験期間: 2024/04/11〜2024/04/15
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

## 生成したアニメのサンプル (24frame,8fps)
### Reagional Prompter 有効時
#### サンプル
* ![Sample01](SampleAnimations/00016-3418874118.webp)
* ![Sample02](SampleAnimations/00152-752436473.webp)
* ![Sample03](SampleAnimations/00218-1320549600.webp)
#### Prompt 及び AnimateDiff の設定
* https://raw.githubusercontent.com/SuperHimoYarouWorld/UseAnimateDiffPromptTravelwithRegionalPrompterSample/main/SampleAnimations/00016-3418874118.txt
* https://raw.githubusercontent.com/SuperHimoYarouWorld/UseAnimateDiffPromptTravelwithRegionalPrompterSample/main/SampleAnimations/00152-752436473.txt
* https://raw.githubusercontent.com/SuperHimoYarouWorld/UseAnimateDiffPromptTravelwithRegionalPrompterSample/main/SampleAnimations/00218-1320549600.txt
#### 以下はテスト時の Regional Prompter の設定
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

## どうやるの?
### Stable Diffusion Web UI の場合
下の3つの機能拡張を有効化し、サンプルを参考にいい感じのプロンプトを書く。Stable Diffusion の Check Point や AnimateDiff の MotionModule の組み合わせによって Regional Prompter の効き具合が大きく変化する様だ。ところで厳密な演技となるようプロンプトをチューンするのも楽しいが、シーン毎のプロンプトを短めにして AI の解釈に委ねると面白いかも。
* AnimateDiff extension
* * https://github.com/continue-revolution/sd-webui-animatediff
* Dynamic Prompts extension
* * https://github.com/adieyal/sd-dynamic-prompts
* Regional Prompter extension
* * https://github.com/hako-mikan/sd-webui-regional-prompter
### Web UI forge の場合
下の3つの機能拡張を有効化し、サンプルを参考にいい感じのプロンプトを書く。
* AnimateDiff extension (for forge)
* * https://github.com/continue-revolution/sd-forge-animatediff
* Dynamic Prompts extension
* * https://github.com/adieyal/sd-dynamic-prompts
* Regional Prompter extension
* * https://github.com/hako-mikan/sd-webui-regional-prompter
