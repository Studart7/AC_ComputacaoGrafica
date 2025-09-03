
### 2. Processamento de Imagens

# Processamento de Imagens

##  Definição
Processamento de Imagens trata da **manipulação de imagens digitais** para melhoria, extração de características ou preparação para análise. Foca mais em transformações matemáticas e algorítmicas sobre a imagem.

##  Aplicações Comuns
- Remoção de ruído e realce de contraste
- Filtros e bordas (detecção de contornos)
- Compressão e segmentação
- Pré-processamento para visão computacional

##  Características Técnicas
- Filtros espaciais: blur, sharpen, sobel
- Transformações: histograma, FFT
- Operações morfológicas: erosão, dilatação
- Limiarização e segmentação

##  Ferramentas Usuais
- OpenCV
- PIL (Python Imaging Library)
- scikit-image
- MATLAB (Image Processing Toolbox)

## ▶️ Exemplo de Código
Aplicar filtro de desfoque e detector de bordas com OpenCV:
```python
import cv2

img = cv2.imread('imagem.jpg', 0)
blur = cv2.GaussianBlur(img, (5,5), 0)
edges = cv2.Canny(blur, 50, 150)

cv2.imwrite('bordas.jpg', edges)
