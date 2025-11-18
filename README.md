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

