# USAGE

## Use Python Module through terminal

To use the module without using the GUI, you can just use the following command:

````shell script
  python blanket_clusterer_path model_type num_clusters embeddings_path names_path num_items max_depth output_path group_names_path
````

Arguments and descriptions:
<table>
    <thead>
        <tr>
            <th>
                Argument
            </th>
            <th>
                Description
            </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
                <code>blanket_clusterer_path</code>
            </td>
            <td>
                Path to location of <code>main.py</code> in the module
            </td>
        </tr>
        <tr>
            <td>
                <code>model_type</code>
            </td>
            <td>
                Type of clustering algorithm (Supported values: <code>k-means</code>, <code>agglomerative</code>, <code>birch</code> and <code>dbscan</code>)
            </td>
        </tr>
        <tr>
            <td>
                <code>num_clusters</code>
            </td>
            <td>
                Number of clusters in a certain level of the hierarchy
            </td>
        </tr>
        <tr>
            <td>
                <code>embeddings_path</code>
            </td>
            <td>
                Absolute path to <code>Word2Vec</code> model
            </td>
        </tr>
        <tr>
            <td>
                <code>names_path</code>
            </td>
            <td>
                Absolute path to the names file (file must be in a specific format, check out [INSERT PAGE LINK])
            </td>
        </tr>
        <tr>
            <td>
                <code>num_items</code>
            </td>
            <td>
                Number of entities a cluster should have
            </td>
        </tr>
        <tr>
            <td>
                <code>max_depth</code>
            </td>
            <td>
                Maximum depth of hierarchy (Current maximum supported depth is 6)
            </td>
        </tr>
        <tr>
            <td>
                <code>output_path</code>
            </td>
            <td>
                Absolute path to the <code>output.json</code> file 
            </td>
        </tr>      
        <tr>
            <td>
                <code>group_names_path</code>
            </td>
            <td>
                Absolute path to the group names file (This file is <strong>optional</strong>, but provides better visualization. 
                The format needs to be the same as <code>names_path</code> file)
            </td>
        </tr> 
    </tbody>
</table>

**If any errors occur, you should be notified through the terminal.**

After successfully executing the shell command, you should see your `output.json` file, with the clustered results in it.

It should look something like the following example:
```json
{
  "id": "0",
  "label": "Example Parent 1",
  "coverage": "0.123",
  "groups": [
  {
    "id": "0.0",
    "label": "Example Child 1",
    "coverage": "0.123",
    "groups": [
    {
      "id": "0.0.0",
      "label": "Example Child 3",
      "coverage": "0.123"
    },
    {
      "id": "0.0.1",
      "label": "Example Child 4",
      "coverage": "0.123"
    }]  
  },
  {
    "id": "0.1",
    "label": "Example Child 2",
    "coverage": "0.123"
  }  
]
}
```

You might have noticed the `coverage` attribute. This attribute is used for the coloring part of the visualization and it is only
present if you have provided a `group_names_path` file.

## Use Python Module through GUI

**IMPORTANT: The Web Application (GUI) is the one that provides the 3D visualization. Without it, you can only view the `output.json` file**

After you have downloaded both the Python Module and the Web Application, and setup them according to [Getting Started](../getting-started/getting-started.md) 
you can easily cluster your data following these couple of steps.

### 1. Make sure your Web Application is running (both Flask and ReactJS)

Commands to start up the application: `npm start` for ReactJS and `flask run` for Flask.

Head over to `http://localhost:3000` to access the GUI

### 2. Head over to `Clusterize` on the GUI
![Blanket Clusterer Home Page](../_images/Blanket_Clusterer_HomePage.png)

### 3. Upload the `Word2Vec` model
![Upload Word2Vec](../_images/Blanket_Clusterer_Word2Vec_Upload.png)

### 4. Upload the `names` file
![Upload names](../_images/Blanket_Clusterer_Names_Upload.png)

### 5. Upload the `group_names` file [_OPTIONAL_]
![Upload group names](../_images/Blanket_Clusterer_GroupNames_Upload.png)

### 6. Define clustering parameters
![Define parameters](../_images/Blanket_Clusterer_Parameters.png)

> Check out our example for parameters
> ![Parameters example](../_images/Blanket_Clusterer_Parameters_Example.png)

### 7. Wait a bit while the process is executing


### 8. Check out the results
#### With Group names
![Results with group names](../_images/Blanket_Clusterer_Results_GroupNames.jpg)
#### Without Group names
![Results without group names](../_images/Blanket_Clusterer_Results_NoGroupNames.png)