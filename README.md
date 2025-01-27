# Contribution rules
In order to maintain easy to use community-driven tutorial platform, there are several strict rules we have to follow.

1. Every topic is a unique, simple and permanent folder with a URL-safe name (e.g. "docker")
2. Every topic has a reserved path `_index/_index.yaml`  
`_index.yaml` file contains metadata related to current topic and has following structure (example for "docker" topic):
```yaml
# _index/_index.yaml

# list of related topics for recommended reads (optional)
related_topics:
- kubernetes
- vm

# title of a topic translated to other languages (required)
title:
  i18n:
    # ISO 639-1 language code followed by a translation
    en: Docker
    ru: Docker

# short description of a topic with translation (optional)
description:
  i18n:
    en: Docker is a widely-used open-source tool for containerization...
    ru: Docker — это широко используемый инструмент с открытым исходным кодом для контейнеризации...
```
3. Tutorials have simple, URL-safe and SEO-friendly folder names (e.g. "how-to-create-a-docker-container")
4. Tutorial folder has a reserved metadata `_index.yaml` file with following structure:
```yaml
# _index.yaml

# (optional)
tags:
- docker
- container
```
5. Tutorial folder has a reserved `static/` folder that contains images and other static media content.
6. Statics have following naming convention:  
   `{ISO 639-1 language code}_{"image"/"video"/etc}_{zero-padded number}` (e.g. "en_image_01.png", "zh_image_01.png")
8. The tutorials themselves are stored inside markdown-based files named after ISO 639-1 language codes. (`en.md`, `ru.md`, `zh.md`, etc)

### Example folder structure:

```
tutorials/docker
tutorials/docker/_index/_index.yaml
tutorials/docker/how-to-create-a-docker-container
tutorials/docker/how-to-create-a-docker-container/_index.yaml
tutorials/docker/how-to-create-a-docker-container/static/en_image_01.png
tutorials/docker/how-to-create-a-docker-container/static/zh_image_01.png
tutorials/docker/how-to-create-a-docker-container/en.md
tutorials/docker/how-to-create-a-docker-container/zh.md
```
