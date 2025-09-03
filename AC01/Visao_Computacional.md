
# Visão Computacional

##  Definição
Visão Computacional tem como objetivo permitir que **computadores “vejam” e interpretem imagens e vídeos**, replicando ou superando a percepção visual humana para tomada de decisão automatizada.

##  Aplicações Comuns
- Detecção e rastreamento de objetos
- Reconhecimento facial
- OCR (Reconhecimento de Texto)
- Diagnóstico médico automatizado

##  Características Técnicas
- Uso de redes neurais convolucionais (CNNs)
- Classificação, segmentação, detecção
- Modelos pré-treinados como YOLO, SSD, Faster R-CNN
- Processamento em tempo real ou em lote

##  Ferramentas Usuais
- OpenCV + Deep Learning
- TensorFlow, Keras, PyTorch
- YOLOv5, Detectron2
- Datasets: COCO, ImageNet, OpenImages

## ▶️ Exemplo de Código
Detectar objetos com YOLOv5 (PyTorch):
```bash
# Clonar repositório YOLOv5
git clone https://github.com/ultralytics/yolov5
cd yolov5
pip install -r requirements.txt

# Rodar detecção em imagem
python detect.py --source path/to/image.jpg --weights yolov5s.pt
