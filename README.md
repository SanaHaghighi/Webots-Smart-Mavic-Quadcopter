# 🚁 Webots Smart Mavic Quadcopter


## 🛰️ Overview

This project simulates a **Mavic-style quadcopter** in **Webots R2023b**, designed to navigate over labeled boxes and identify objects using a **Convolutional Neural Network (CNN)** based on the **MNIST Fashion dataset**.  
The drone detects its target, adjusts its flight path, and activates its front LEDs upon successful identification.

📸 **Examples**  

📸 **Example placeholder**  
<img width="350" alt="image" src="https://github.com/user-attachments/assets/1afabf7e-bbc4-4ad0-8a21-e145527c6f4b" />


---

## 🧱 Repository Structure

├── cnn/ → CNN architecture and training scripts

├── controllers/ → Drone flight, camera, and LED control codes

├── datasets/ → MNIST Fashion dataset and preprocessing code

├── images/ → Captured frames and sample results

├── model/ → Webots world and Mavic configuration files

├── videos/ → Simulation recordings and demo outputs

---

## ⚙️ Prerequisites

To successfully run the project, make sure you have:
- Webots R2023b  
- Keras  
- OpenCV (cv2)  
- Pillow (PIL)

Then load the simulation environment:
`mavic_2_pro.wbt`

---

## 🚀 Implementation

We designed a controller to manage drone flight across multiple boxes labeled with MNIST images.  
For each run, the drone receives a **target label** (specific clothing item). It then captures images while hovering above boxes to classify them.

> 📷 
> Example placeholder: <img width="602" height="569" alt="image" src="https://github.com/user-attachments/assets/37843199-c9b4-4e73-b27e-2fe35c254340" />


If the CNN output matches the target label, the drone lands next to the correct box and activates its LED lights.  
If not, it continues searching other boxes until the match is found.

---

## 🎮 Controller

We implemented the controller by testing different values for:
- Speed  
- Flight angles  
- Image capture timing  

Once optimized through trial and error, the controller achieved steady flight and accurate capture.  
For details, refer to Webots documentation on **quadcopter control and command APIs**.

---

## 🧠 CNN Architecture

Since the **MNIST Fashion dataset** includes low-resolution grayscale images, several filters were applied before feeding data into the CNN.  
Edges were enhanced and contrast increased—correcting misclassifications (e.g. confusing bags with boots).  
This improved clarity allowed the model to **correctly predict labels**.

---

## 🎬 Final Result

> 🎥
![Controller Test Preview](videos/controller_test.gif)  


The final simulation demonstrates successful navigation, detection, and LED signaling when the correct item is identified.

---

## 📈 Results Summary

| Metric           | Description           | Value |
|------------------|-----------------------|--------|
| Model Accuracy   | Correct label detection | 92%   |
| Average Flight Time | Per search cycle     | 45 sec |
| Environment Size | 10m x 10m             | - |

> 🪶 *You can adjust metrics after running updated tests.*

---

## 🔩 Future Improvements

- Enhance CNN performance using transfer learning.  
- Integrate real-time camera feed.  
- Test object generalization beyond MNIST Fashion dataset.  
- Optimize LED feedback for multi-target detection.

---

## 📄 License
This project is licensed under the **MIT License**. See `LICENSE` file for details.

---

## 👩‍💻 Authors & Credits

Developed by **Sana Haghighi** and team (2023–2024).  
Guidance: Mavic Quadcopter Object Detection using CNN — Webots Simulation Environment.  

---






