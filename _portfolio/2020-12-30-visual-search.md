---
title: "Fashion Map"
excerpt: "Building a visual search algorithm using CNNs"
header:
#   image: /assets/images/sim_interface.jpg
  teaser: /assets/images/fashion_map.png
sidebar:
  - title: "Responsibilities"
    text: "Model training, project leadership"
  - title: "Tools + Libraries"
    text: "Tensorflow, transfer learning"
  - title: "<a href=\"https://github.com/datascopeanalytics/DeepProduct\">Github Repo</a>"
gallery:
  - url: /assets/images/fashion_map.png
    image_path: /assets/images/fashion_map.png
    alt: "T-SNE map of fashion items"

---
Using latent-space feature vectors from a convolutional neural network (CNN), I built a tool to find visually similar clothing items. Working with some coworkers, we built a tool called "Dope or Nope?" where users could rate whether they thought two items of clothing were similar in order to test multiple distance metrics and feature vectors to find the best performing model on the subjective matching task.

[I wrote about this project for the Datascope blog.](https://datascopeanalytics.com/blog/building-a-visual-search-algorithm/) I also presented this work as a tutorial on CNNs at [Metis](thisismetis.com) and at [Prepare.ai](https://prepare.ai/)

{% include gallery caption="T-SNE mapping of 500 fashion items from the dataset" %}