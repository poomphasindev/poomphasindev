# Phasin “Poom” Petluechai

I teach models to read Thai license plates, odometers and the tiny expiry dates on product labels. I study Computer Engineering & Digital Technology at Chulalongkorn University in Bangkok.

[Kaggle](https://www.kaggle.com/phasinpet) · [LinkedIn](https://www.linkedin.com/in/phasin-petluechai/) · [Email](mailto:poomphasin+work@gmail.com)

### From my experiment log

At Axons, I fine-tuned one model for all three tasks. Here’s how often it got the text exactly right, averaged across tasks on a 673-image internal holdout.

```text
Qwen3-VL-8B       █████████████░░░░░░░   63.41%
+ 4-bit QLoRA     ██████████████████░░   89.03%
```

**One bug worth chasing.** On expiry labels, our Gemini prompt and our annotators used different rules for `LOT` and `SUBLOT`. I rewrote the prompt to match the annotation rule and reran the same 110 images. Fully correct records went from **61 to 102**.

### A few things I’ve built

- **Street View house classifier.** Can you spot a house behind a parked car and a garden fence? I trained ConvNeXtV2 on 2,953 street scenes to answer that one-bit question. [Code & confusion matrix](https://github.com/poomphasindev/House_Recognition_SupAIss6)
- **Vehicle recognition on a Jetson Nano.** I led the model team that paired YOLO detection with MobileNetV3 classification and ran both on-device in real time. We won the Edge-AI for Intelligent Transport System Hackathon.
- **Invoice reader for UBE Chemicals.** I used the positions of words on the page to pair invoice numbers, dates and purchase orders with their labels. Each page in the annotation set can be traced back to its source file.

<sub>Usually running on Python, PyTorch and hotpot.</sub>
