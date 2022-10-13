<!-- ---
title: 🏡 Главная
permalink: /
nav_order: 1
---

# Введение в машинное обучение
Курс представляет собой изложение современных результатов и подходов в решении прикладных задач оптимизации. Несмотря на фокус на приложения, курс содержит необходимый набор теоретических основ для того, чтобы понимать почему и как определенные методы работают. 

[✅ Вступительное тестирование](/intro_test)

Каждое занятие состоит из 2-3 практикумов (30-45 минут теории + 30-45 минут самостоятельной интерактивной работы). Успешное выполнение заданий на практикумах гарантирует прохождение курса.

* [🚀 Программа](/program)
* [🧠 Слушатели](/students)
* [📧 Чат](https://t.me/+vEZLTQ9wWT44OTRi)
* [📧 Канал](https://t.me/+vEZLTQ9wWT44OTRi)
* [👨‍💻 Github](https://github.com/Arseny5/Arseny5.github.io)


| Иванов Арсений | Калязин Николай | Братчиков Сергей | Даниил Волков |
| ------------ | ------------- | ------------- | ------------- |
| <img src="1.jpg" width="250"> | <img src="3.jpg" width="250"> | <img src="4.jpg" width="250"> | <img src="2.jpg" width="250">  |
| SberAI <br> Tg: https://t.me/arsmathprog <br> Tg-канал: <https://t.me/ivarsivars> | LevshAI <br> Tg:  https://t.me/FanatBoba  |  University 20.35 <br> Tg:  https://t.me/hivaze  | RTLabs <br> Tg:  https://t.me/wolf_Da |

Октябрь, 2022 г. -->

---
title: ONNX Runtime
description: ONNX Runtime is a cross-platform machine-learning model accelerator
has_children: false
nav_order: 0
redirect_from: /how-to
---

# Welcome to ONNX Runtime
{: .no_toc }

ONNX Runtime is a cross-platform machine-learning model accelerator, with a flexible interface to integrate hardware-specific libraries. ONNX Runtime can be used with models from PyTorch, Tensorflow/Keras, TFLite, scikit-learn, and other frameworks.

<iframe height="315" class="table-wrapper py px" src="https://www.youtube.com/embed/DwdAqoyyzhI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## How to use ONNX Runtime

|:----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
|  <span class="fs-5"> [Get started with ORT](./get-started){: .btn  .mr-4 target="_blank"} </span> |  <span class="fs-5"> [API Docs](./api){: .btn target="_blank"} </span>      |
| <span class="fs-5"> [Tutorials](./tutorials){: .btn target="_blank"} </span>                     |   <span class="fs-5"> [Ecosystem](./ecosystem){: .btn target="_blank"} </span>                          | 
| <span class="fs-5">[ONNX Runtime YouTube](https://www.youtube.com/channel/UC_SJk17KdRvDulXz-nc1uFg/featured){: .btn  .mr-4 target="_blank"} </span>         | 

## Contribute and Customize

|:----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
|  <span class="fs-5"> [Build ORT Packages](./build){: .btn  .mr-4 target="_blank"} </span>| <span class="fs-5">[ONNX Runtime GitHub](https://github.com/microsoft/onnxruntime){: .btn target="_blank"} </span>  | 


---

## QuickStart Template

|:----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
|  <span class="fs-5"> [ORT Web JavaScript Site Template](https://github.com/microsoft/onnxruntime-nextjs-template){: .btn  .mr-4 target="_blank"} </span>         |  <span class="fs-5"> [ORT C# Console App Template](https://github.com/microsoft/onnxruntime-csharp-cv-template){: .btn  .mr-4 target="_blank"} </span>         | 


---


## ONNX Runtime for Inferencing

ONNX Runtime Inference powers machine learning models in key Microsoft products and services across Office, Azure, Bing, as well as dozens of community projects.

Examples use cases for ONNX Runtime Inferencing include:

* Improve inference performance for a wide variety of ML models
* Run on different hardware and operating systems
* Train in Python but deploy into a C#/C++/Java app
* Train and perform inference with models created in different frameworks

### How it works
{: .no_toc }

The premise is simple. 
1. **Get a model.** This can be trained from any framework that supports export/conversion to ONNX format. See the [tutorials](./tutorials) for some of the popular frameworks/libraries. 
2. **Load and run the model with ONNX Runtime.** See the [basic tutorials](./tutorials/api-basics) for running models in different languages.
3. ***(Optional)* Tune performance using various runtime configurations or hardware accelerators.** There are lots of options here - see [How to: Tune Performance](./performance/tune-performance.md) as a starting point.

Even without step 3, ONNX Runtime will often provide performance improvements compared to the original framework. 

ONNX Runtime applies a number of graph optimizations on the model graph then partitions it into subgraphs based on available hardware-specific accelerators. Optimized computation kernels in core ONNX Runtime provide performance improvements and assigned subgraphs benefit from further acceleration from each [Execution Provider](./execution-providers).



---

## ONNX Runtime for Training

Released in April 2021, ONNX Runtime Training provides a one-line addition for existing PyTorch training scripts to accelerate training times. The current support is focused on large transformer models on multi-node NVIDIA GPUs, with more to come. 

### How it works
{: .no_toc }

Using the ORTModule class wrapper, ONNX Runtime for PyTorch runs the forward and backward passes of the training script using an optimized automatically-exported ONNX computation graph. ORT Training uses the same graph optimizations as ORT Inferencing, allowing for model training acceleration. 

The ORTModule is instantiated from [`torch-ort`](https://github.com/pytorch/ort) backend in PyTorch. This new interface enables a seamless integration for ONNX Runtime training in a PyTorch training code with minimal changes to the existing code.


