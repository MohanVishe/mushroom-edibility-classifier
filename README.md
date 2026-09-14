# 🍄 Mushroom Edibility Classifier

**Classifying mushrooms as edible or poisonous from their physical characteristics.**

> ### ⚠️ Status: incomplete
>
> This was started as a full MLOps project — modular `src/` package, training and
> prediction pipelines, logging, custom exceptions. **The scaffold was created but
> never filled in.** Every module under `src/` is an empty file.
>
> What actually exists and works is the research notebook:
> [`notebooks/research.ipynb`](notebooks/research.ipynb) — data exploration and
> model experimentation on the UCI mushroom dataset.
>
> It's kept public rather than deleted because the exploratory analysis is real and
> the abandoned structure is an honest record of scope I set and didn't finish.
> If you're here from my profile, the finished work is in
> [medical-rag-chatbot](https://github.com/MohanVishe/medical-rag-chatbot),
> [pdf-parser-benchmark](https://github.com/MohanVishe/pdf-parser-benchmark) and
> [rossmann-sales-forecasting](https://github.com/MohanVishe/rossmann-sales-forecasting).

---

## What's here

```
├── notebooks/
│   ├── research.ipynb          # ✅ the real content — EDA and modelling
│   └── data/mushrooms.csv      # UCI mushroom dataset, 8,124 samples
├── src/MushroomSafetyPredictor/
│   ├── components/             # ⬜ empty
│   ├── pipelines/              # ⬜ empty
│   ├── logger.py               # ⬜ empty
│   └── exception.py            # ⬜ empty
├── requirements/
├── init_setup.sh
└── setup.py
```

## The dataset

The [UCI Mushroom dataset](https://archive.ics.uci.edu/dataset/73/mushroom) — 8,124 samples
described by 22 categorical features (cap shape, odour, gill size, spore print colour and so on),
each labelled edible or poisonous.

It's a well-known dataset with an unusual property: it is **almost perfectly separable**. A single
feature, odour, classifies the majority of samples on its own, and most classifiers reach near-100%
accuracy without effort. That makes it a good teaching set for pipelines and a poor one for
comparing models — which is worth knowing before reading too much into any accuracy number from it.

## To finish this

The remaining work, in order:

1. Move the notebook logic into `src/components/` — data ingestion, transformation, model trainer
2. Implement `logger.py` and `exception.py` (both currently empty)
3. Wire up `pipelines/training_pipeline.py` and `pipelines/prediction_pipeline.py`
4. Add DVC for data versioning and MLflow for experiment tracking
5. Containerise and deploy

## License

MIT
