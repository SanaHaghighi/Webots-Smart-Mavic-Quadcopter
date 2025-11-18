# Webots Smart Mavic Quadcopter  
**Guidance of a Quadcopter for Object Detection**

---

## 🛰️ Overview

This project simulates a **Mavic-style quadcopter** in **Webots R2023b**, designed to navigate over labeled boxes and identify objects using a **Convolutional Neural Network (CNN)** based on the **MNIST Fashion dataset**.  
The drone detects its target, adjusts its flight path, and activates its front LEDs upon successful identification.

> 📸
> Example placeholder:<img width="1110" height="606" alt="image" src="https://github.com/user-attachments/assets/5431b1bc-299c-4cd5-a78b-e30131b9b3b2" />


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

To successfully run the project, you need to install:

Webots R2023b

Keras

OpenCV (cv2)

PIL

Then load the simulation environment:

mavic_2_pro.wbt


---

## 🚀 Implementation

We designed a controller to manage drone flight across multiple boxes labeled with MNIST images.  
For each run, the drone receives a **target label** (specific clothing item). It then captures images while hovering above boxes to classify them.

> 📷 *Upload the drone flight environment screenshot here.*  
> (Example placeholder: `![Flight Environment](INSERT_IMAGE_LINK_HERE)`)

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

> 🖥️ *Upload a short clip or image showing controller operation here.*  
> (Example placeholder: `![Controller Test](INSERT_IMAGE_LINK_HERE)`)

---

## 🧠 CNN Architecture

Since the **MNIST Fashion dataset** includes low-resolution grayscale images, several filters were applied before feeding data into the CNN.  
Edges were enhanced and contrast increased—correcting misclassifications (e.g. confusing bags with boots).  
This improved clarity allowed the model to **correctly predict labels**.

> 🧩 *Upload an image of CNN layers or confusion matrix here (optional).*  
> (Example placeholder: `![CNN Visualization](INSERT_IMAGE_LINK_HERE)`)

---

## 🎬 Final Result

> 🎥 *Upload your simulation video here.*  
> (Example placeholder:  
> `[▶ Watch Quadcopter Object Detection Demo](INSERT_VIDEO_LINK_OR_PATH_HERE)`)

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

Developed by **Sana Haghighi** and team (2024–2025).  
Guidance: Mavic Quadcopter Object Detection using CNN — Webots Simulation Environment.  

> 💫 *If part of an academic paper or presentation, add citation details here.*

---

## 💬 Contact  
For more details, discussions, or collaboration:  
📧 `sanahaghighi@github.com`  
🔗 [GitHub Profile](https://github.com/SanaHaghighi)

---
