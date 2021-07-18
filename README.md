# Optimal-Positioning-of-text


* I have used basNET for differentiating the background from the foreground.
* Background pixels are closer to [255,255,255] and foreground are closer to [0,0,0] using this property I converted all the pixels based on their Euler distances from these pixels.
* Then used these pixels values completely remove the foreground image so the mean shift algorithm can be applied only on the background image.
* I used the sklearn.cluster libraries mean shift algorithm. I got a result that looks reasonable. But the time it is taking is too much. Need to search for some better implementation.
* Regarding searching for the maximized space, I was thinking of using DFS to calculate the number of pixels that have approximately the same pixel values. 
* Once we get values of the region for all components we can take one with maximum area.
* One noticeable problem in this approach is that the region with the maximum area may not be in rectangular or some reasonable shape. 
* So if there is some built-in library to do this, it will be easy. I need to see if there exists one.

These are some results of the model.

## Original Image

![image](https://user-images.githubusercontent.com/59763897/126057590-f41c740d-0390-4a86-97ac-c8a3bff850a0.png)


## BasNET output:

![image](https://user-images.githubusercontent.com/59763897/126057598-5160bb17-8872-408e-8596-f1cfcb643553.png)


## Only background Image:

![image](https://user-images.githubusercontent.com/59763897/126057601-30b304bb-6335-4c75-89b5-1b128b8664ec.png)



## Output of mean shift algorithm

![image](https://user-images.githubusercontent.com/59763897/126057609-da96ae9e-e451-45b9-91ce-93489de45d37.png)


## How to run

Use the code mentioned in Imageprocessing.ipynb to execute. Run the cells one after the other. As of now I have used the code for individal part from other resources. But we will specialize them very soon.
