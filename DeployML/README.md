## Домашняя работа к занятию “Deply ML”
## **Цель задания**

Закрепить полученные знания и научиться настраивать PyTorch посредством настройки окружения и проведения обучения модели c использованием torchserve-dashboard

## **Задание**:

1. Склонировал https://github.com/pytorch/serve
2. Запустил python ./ts_scripts/install_dependencies.py
3. Установил библиотеки pip install torchserve torch-model-archiver torch-workflow-archiver
4. склонировал git clone https://github.com/pytorch/serve.git
5. Создал папку mkdir model_store
6. Скачал модель wget https://download.pytorch.org/models/densenet161-8d451a50.pth
6. Заархивируйте модель с помощью архиватора моделей. torch-model-archiver --model-name densenet161 --version 1.0 --model-file ./serve/examples/image_classifier/densenet_161/model.py --serialized-file densenet161-8d451a50.pth --export-path model_store - -extra-files ./serve/examples/image_classifier/index_to_name.json --handler image_classifier
8. Установил pip install torchserve-dashboard
6. Стартуем сервер из под torchserve-dashboard с параметром
--config_path ./torchserve.properties --model_store ./model_store --server.port 8501 -- --config_path ./torchserve.properties
   