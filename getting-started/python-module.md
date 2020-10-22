# Python Module

## Setup

The python module will be ready to use, as soon as you install the necessary requirements
using `pip`, as shown:

```shell script
pip3 install -r requirements.txt
```

After installing the requirements, the module is ready for usage.
You could use it through a **terminal**, or you could use the [Web Application](web-application.md).

## How to use through Terminal

To use the module without using the GUI, you can just use the following command:

````shell script
  python blanket_clusterer_path model_type num_clusters embeddings_path names_path num_items max_depth output_path group_names_path
````

The ``group_names_path`` argument is optional, but is advisable to use it for better visualization results.