# pytorch-segmentation-template

This is a **baseline template for semantic segmentation tasks** (you can easily customize for other tasks) based on [https://github.com/victoresque/pytorch-template](https://github.com/victoresque/pytorch-template). Although based on the mentioned template, many things are modified to make it easier and more intuitive to follow. The modifications are,

1. Segmentation models are from [https://github.com/qubvel/segmentation_models.pytorch](https://github.com/qubvel/segmentation_models.pytorch) which provides a variety of models including `timm`.

2. `test_config.json` is added along with the original `config.json` so that both training and inference can be done with config files. `config.json` is responsible for training and `test_config.json` is responsible for inference.

3. Removed the complicated **inheritance** structure and replaced with simple and intuitive folder structures.

4. Complete modularization: Each module is responsible for one thing only.

5. Support `COCO` format datasets: Just provide the coco-format `.json` files and you're set.

# Folder Structure

```
📦pytorch-segmentation-template
 ┣ 📂data_loader
 ┃ ┣ 📜dataloader.py
 ┃ ┗ 📜dataset.py
 ┣ 📂logger
 ┃ ┣ 📜__init__.py
 ┃ ┣ 📜logger.py
 ┃ ┗ 📜logger_config.json
 ┣ 📂loss
 ┃ ┣ 📜__init__.py
 ┃ ┗ 📜losses.py
 ┣ 📂metric
 ┃ ┣ 📜__init__.py
 ┃ ┣ 📜metric_tracker.py
 ┃ ┗ 📜metrics.py
 ┣ 📂models
 ┃ ┗ 📜build_smp_model.py
 ┣ 📂trainer
 ┃ ┣ 📜__init__.py
 ┃ ┗ 📜trainer.py
 ┣ 📂utils
 ┃ ┣ 📜__init__.py
 ┃ ┗ 📜utils.py
 ┣ 📜README.md
 ┣ 📜config.json
 ┣ 📜config_parser.py
 ┣ 📜inference.py
 ┣ 📜test_config.json
 ┣ 📜train.py
 ┗ 📜train.sh
```

Any feedbacks are welcome!