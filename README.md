# Summary of Work Done Using DINO Model

## Objective:
Enhance the recognition and understanding of micro and macro features of sign language gestures using the self-attention mechanisms of the DINO model.

## Models Utilized:
- **DINO ResNet 50**
- **DINO Small 8x8**
- **DINO Small 16x16**
- **DINO Base 8x8**
- **DINO Base 16x16**

## Approach:
1. **Model Utilization**:  
   Employed the DINO model (5 flavors), designed for self-supervised learning, to focus on learning from visual data without requiring detailed annotations.
   
2. **Attention Mechanism Exploration**:  
   Used the multi-head attention mechanism of the model to analyze specific parts of the hand gestures in sign language.

## Implementation Details:
- **Image Processing**:  
  Transformed images of hand gestures to fit the model’s input requirements, including normalization and resizing to match the model’s patch size.

- **Attention Map Extraction**:  
  Extracted self-attention maps from the model for each image to visualize the focus areas, implemented for multiple heads to capture different features emphasized by each head.

- **Visualization**:  
  Visualized the attention maps to assess the model’s focus areas, using individual attention maps for each head and a combined mean attention map to summarize overall focus areas across heads.

## Results:
- **Focused Attention**:  
  The attention visualizations show the model focusing on relevant features of the sign language gestures, especially around the hand areas.

- **Head Variation**:  
  Visualizations from different attention heads show varying focus points, indicating that the model captures a diverse set of features from the same input, enriching the analysis and understanding of the gestures.

## Model Details

### DINO ResNet-50:
The **DINO ResNet-50** model is a convolutional neural network (CNN)-based architecture designed for self-supervised learning. ResNet-50 uses **convolutions** and **pooling layers** to process images hierarchically, allowing it to detect various features at different levels of abstraction (e.g., edges, textures, and objects).

**Key Characteristics:**
- ResNet-50 excels at extracting hierarchical features but does **not** include an attention mechanism like transformer-based models.
- It generates **feature maps** that represent activations of learned features across spatial regions of the image, though without the explicit focus of attention maps.

![Visualization of attention maps of Dino_resnet50](https://prod-files-secure.s3.us-west-2.amazonaws.com/5dfa7e63-6032-4d84-bead-312aba22a447/0368043e-0710-46ae-8e65-81f7944e08aa/image.png)

---

### DINO Small:
The **DINO Small** models (ViT-S/8 and ViT-S/16) demonstrated strong capabilities in focusing on important features in images, particularly around the hand gestures.

**Key Characteristics:**
- **ViT-S/8** (with 8x8 patches) produces more **detailed** attention maps, focusing on finer aspects of the gestures like finger positioning.
- **ViT-S/16** (with 16x16 patches) offers a more **global** view, sacrificing some detail for computational efficiency.
- Both models showed a distributed focus across multiple attention heads, emphasizing different levels of detail and the overall hand structure.

![Visualization of attention maps of Dino_Small_8 for five Irish Sign Language hand signs](https://prod-files-secure.s3.us-west-2.amazonaws.com/5dfa7e63-6032-4d84-bead-312aba22a447/fd7afffa-f02f-4a6a-80c3-6ba6166f8c12/download_(1).png)

![Visualization of attention maps of Dino_Small_16 for five Irish Sign Language hand signs](https://prod-files-secure.s3.us-west-2.amazonaws.com/5dfa7e63-6032-4d84-bead-312aba22a447/f5990483-d724-476d-b802-1fdcf203c0a9/download_(1).png)

---

### DINO Base:
The **DINO Base** models (ViT-B/8 and ViT-B/16) with larger architectures captured more **refined** and **detailed** spatial features. These models excel at identifying both **fine-grained** and **broader** aspects of hand gestures.

**Key Characteristics:**
- The **DINO Base** models demonstrated sophisticated attention, with **ViT-B/16** capturing larger, coarser features, while **ViT-B/8** zoomed into intricate hand motions.
- These models proved highly suitable for hand gesture recognition tasks, showcasing their ability to differentiate various hand shapes and movements.

![Visualization of attention maps of Dino_base_8 for five Irish Sign Language hand signs](https://prod-files-secure.s3.us-west-2.amazonaws.com/5dfa7e63-6032-4d84-bead-312aba22a447/cf9b78a8-d176-4784-aa76-cbcbd138d54b/download_(1).png)

![Visualization of attention maps of Dino_base_16 for five Irish Sign Language hand signs](https://prod-files-secure.s3.us-west-2.amazonaws.com/5dfa7e63-6032-4d84-bead-312aba22a447/c4cf7fb7-1f63-432e-a0a8-6b8bba30355e/download.png)

---

## Conclusion:
The application of the DINO model’s self-attention mechanism on sign language gesture images successfully highlights critical areas and features, demonstrating the model’s potential to focus on and interpret sign language effectively based solely on visual cues.

