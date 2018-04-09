---
layout: post
title: Azkaban Notes
categories: Big_data
description: Azkaban入门知识
keywords: big_data, Azkaban
---

## Installation

### Solo server mode

Follow these steps to get started. 
 
* **Clone the repo:** run git clone https://github.com/azkaban/azkaban.git  
* **Build Azkaban and create an installation:** run cd azkaban; ./gradlew build installDist  
* **Start the server:** run cd azkaban-solo-server/build/install/azkaban-solo-server; bin/azkaban-solo-start.sh  
* **Stop server:** run bin/azkaban-solo-shutdown.sh from within the azkaban-solo-server installation directory  

UI: localhost:8081  default usr/pwd: Azkaban/Azkaban



## Upload Tasks

Example

~~~
# cat ./task1.job
type = command  
command = chmod +x main  

# cat ./task2.job
type = command
command = ./main
dependencies = task1
~~~

* One job can only run single command line.
* You can write into one single shell for all your commands. 



