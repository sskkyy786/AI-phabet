# Week 5 

Welcome to the concluding week of our project

*This part is entirely optional, so feel free to skip unless curiosity has the best of you.*

Now, we're diving into the testing phase with our own data, and there are two avenues to explore:

1. **Drawing UI Method:**

   Employ a drawing app to craft characters, integrating them into the trained model. This approach allows us to assess the model's performance when confronted with hand-drawn inputs.

3. **Camera-Captured Text:**

   Capture text images using a camera and input them into the model. This method provides a real-world evaluation, showcasing how well our model handles diverse, dynamically captured data.

Feel at liberty to delve into either or both of these methods, depending on your curiosity and interest in the final phases of the project.

---

## Camera-Captured Text

We'll employ OpenCV for preprocessing our drawn characters and camera-captured data. (OpenCV (Open Source Computer Vision Library), excels at image processing tasks, offering robust capabilities for tasks like resizing, filtering, and enhancing images. Its use here ensures efficient data preprocessing before input to the trained model.)

Here are some valuable materials to enhance your understanding of OpenCV:
- Watch [this video](https://www.youtube.com/watch?v=oXlwWbU8l2o) by freeCodeCamp for a comprehensive introduction to OpenCV.
- Refer to the official OpenCV [documentation](https://docs.opencv.org/4.x/d6/d00/tutorial_py_root.html). (Remember you never need to completely understand the complete documentation/code of any library, but you should have some idea of it so you can refer to it in time of need).
- Our character extraction task heavily relies on the contour function of OpenCV, covered in the aforementioned video lecture. For additional insights, check out [this video](https://www.youtube.com/watch?v=WEzfqCTeI5E).

Additionally, here's a [link](https://colab.research.google.com/drive/1tdaAxwxceUl8PYbtsj1YQqBy5672FpEG?authuser=0#scrollTo=QGQTbjzq_4Be) to a Colab file providing a rough walkthrough that you might find helpful.

## Drawing UI

 For this method, we'll use the pygame library due to its ease of creating a user interface that facilitates live character drawing and subsequent feeding to the trained model. Pygame provides a simple and efficient way to handle graphical user interfaces, making it an ideal choice for our purpose.

Pygame is a relatively simple library, making it an easy task to learn. 
- If you prefer learning by watching, you can check out [this video](https://www.youtube.com/watch?v=AY9MnQ4x3zk&t=3088s) (only till 2:23:50 is necessary; feel free to skip the rest) to see pygame being implemented.
- For more in-depth information, refer to the Pygame [documentation](https://www.pygame.org/docs/).

You can reach out to me (Pranjal) if you want to try this part out and need more assistance.

---

That wraps up this project!

I hope you've enjoyed the learning journey! If you have any questions or thoughts, feel free to share. 
