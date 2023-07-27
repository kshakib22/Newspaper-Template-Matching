# Newspaper Template Matching
## Overview
The notebook uses template matching to retrieve Shipping report from the Star of Chile newspapers. We observed that shipping reports appear right before the 'Charters' section of the newspaper column. we use that fact to first match the shipping report title followed by the Charters title and crop the portion in between to get our desired table. 
## Guidelines
Firstly, all the images should be **converted in analogous manner**, keeping the dpi and other settings same. This conversion is first done in the main notebook. The template matching algorithm takes in two templates to search for. These templates should also be cropped from the converted images to keep similar settings as the input image for the template image. 
The threshold value is the similarity values found between the template image and different parts of the input image. This value ranges from 0-1 where a value closer to 1 means the portion of interest is very similar to the template provided. For the threshold values used in the matching, it is highly sensitive to different lighting and opacity of the input image/template. The threshold value for comparison (ideal match within the notebook) is found through trial and error by providing positive input images (i.e. images actually containing shipping report within its contents). We can keep the template same for a specific folder, but it is advised to go through a couple of trial and error for different folders (as they may be scanned under different settings). The notebook here works for files in folder **PE0001107**. To work with files of different year/folder such as **PE0001106**, please _adjust threshold values_ accordingly.


## Templates
Our second template, the title 'Charters' was kept same throughout different folders (only threshold values were adjusted). The image used was this : ![template2](https://github.com/kshakib22/Newspaper-Template-Matching/blob/f2185ace52e759e9910da363ce8fc76d89312eb9/template%202.jpg)

At the beginning, our first template was this title : ![old_template1](https://github.com/kshakib22/Newspaper-Template-Matching/blob/f2185ace52e759e9910da363ce8fc76d89312eb9/old%20template%201.jpg) . This had threshold values that varied quite frequently and yielded inaccurate results.

However, the following template yielded the best results: ![new_template1](https://github.com/kshakib22/Newspaper-Template-Matching/blob/f2185ace52e759e9910da363ce8fc76d89312eb9/template%201.jpg) due to its unique nature within the newspaper.
