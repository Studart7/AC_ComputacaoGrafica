# Computação Gráfica

##  Definição
A Computação Gráfica é a área da computação responsável pela **criação e manipulação de imagens geradas por computador**. Envolve desde desenhos 2D até modelagens e renderizações 3D realistas, utilizadas em jogos, filmes, engenharia e simulações.

##  Aplicações Comuns
- Animações e filmes (ex: Pixar)
- Jogos 3D (Unity, Unreal Engine)
- Modelagem CAD/CAE
- Simulações visuais

##  Características Técnicas
- Uso de **malhas (meshes)**, **texturas**, **luzes** e **câmeras virtuais**
- Renderização **em tempo real** (OpenGL/WebGL) ou **offline** (Blender, V-Ray)
- Técnicas de **sombreamento**, **ray tracing**, **oclusão**, etc.

##  Ferramentas Usuais
- Blender (com Python API)
- OpenGL / WebGL
- Unity, Unreal Engine
- Three.js (para web)

## ▶️ Exemplo de Código
Renderizar uma cena 3D com cubo + luz + câmera no Blender com script Python:
```python
import bpy

bpy.ops.mesh.primitive_cube_add()
bpy.context.object.location = (0, 0, 1)
bpy.ops.object.light_add(type='POINT', location=(5, 5, 5))
bpy.ops.object.camera_add(location=(7, -7, 5), rotation=(1.1, 0, 0.7))
bpy.context.scene.render.filepath = '/tmp/render.png'
bpy.ops.render.render(write_still=True)
