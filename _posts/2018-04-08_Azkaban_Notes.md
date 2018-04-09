---
layout: post
title: Azkaban Notes
categories: [big_data]
description: http://azkaban.github.io/azkaban/docs/latest/
keywords: big_data, Azkaban
---

#Azkaban Note

## Installation

### Solo server mode

Follow these steps to get started. 
 
* **Clone the repo:** run git clone https://github.com/azkaban/azkaban.git  
* **Build Azkaban and create an installation:** run cd azkaban; ./gradlew build installDist  
* **Start the server:** run cd azkaban-solo-server/build/install/azkaban-solo-server; bin/azkaban-solo-start.sh  
* **Stop server:** run bin/azkaban-solo-shutdown.sh from within the azkaban-solo-server installation directory  

