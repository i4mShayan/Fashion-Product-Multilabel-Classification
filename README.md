# Fashion Product Multilabel Classification

# Finding the Ideal Base Model
<table>
  <thead>
    <tr>
      <th>Model</th>
      <th>Accuracy</th>
      <th>Precision & Recall</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <strong><em>Base Model:</em></strong> <code>InceptionV3</code><br>
        <strong><em>Epochs:</em></strong> <code>100</code><br>
        <strong><em>Augmentation:</em></strong> <code>No</code><br>
        <strong><em>Learning Rate:</em></strong> <code>1e-5</code><br>
        <strong><em>Optimizer:</em></strong> <code>SGD</code><br>
        <strong><em>Momentum:</em></strong> <code>0.9</code><br>
        <strong><em>Batch Size:</em></strong> <code>32</code><br>
        <strong><em>Regularization:</em></strong> <code>No</code><br>
        <strong><em>Input Resolution:</em></strong> <code>Low</code>
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/4db8144d-a452-4361-860f-248b7766ec8b" alt="Accuracy" width="300" height="200">
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/5b172a36-d6a9-42eb-9f1c-340c1757e386" alt="Precision Recall" width="300" height="200">
      </td>
    </tr>
    <tr>
      <td>
        <strong><em>Base Model:</em></strong> <code>EfficientNetB0</code><br>
        <strong><em>Epochs:</em></strong> <code>100</code><br>
        <strong><em>Augmentation:</em></strong> <code>No</code><br>
        <strong><em>Learning Rate:</em></strong> <code>1e-5</code><br>
        <strong><em>Optimizer:</em></strong> <code>SGD</code><br>
        <strong><em>Momentum:</em></strong> <code>0.9</code><br>
        <strong><em>Batch Size:</em></strong> <code>32</code><br>
        <strong><em>Regularization:</em></strong> <code>No</code><br>
        <strong><em>Input Resolution:</em></strong> <code>Low</code>
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/6ff3fc06-da45-41fe-a32c-ef1457553091" alt="Accuracy" width="300" height="200">
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/df630c03-3eac-4c6d-96ca-d3f6896c0013" alt="Precision Recall" width="300" height="200">
      </td>
    </tr>
    <tr>
      <td>
        <strong><em>Base Model:</em></strong> <code>VGG-16</code><br>
        <strong><em>Epochs:</em></strong> <code>100</code><br>
        <strong><em>Augmentation:</em></strong> <code>No</code><br>
        <strong><em>Learning Rate:</em></strong> <code>1e-5</code><br>
        <strong><em>Optimizer:</em></strong> <code>SGD</code><br>
        <strong><em>Momentum:</em></strong> <code>0.9</code><br>
        <strong><em>Batch Size:</em></strong> <code>32</code><br>
        <strong><em>Regularization:</em></strong> <code>No</code><br>
        <strong><em>Input Resolution:</em></strong> <code>Low</code>
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/6b3491b8-bc6f-4e4f-88fc-3b4b960c56ac" alt="Accuracy" width="300" height="200">
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/dc841512-ad1c-4d33-85d3-d4849c2dc42d" alt="Precision Recall" width="300" height="200">
      </td>
    </tr>
    <tr>
      <td>
        <strong><em>Base Model:</em></strong> <code>ResNet-50</code><br>
        <strong><em>Epochs:</em></strong> <code>100</code><br>
        <strong><em>Augmentation:</em></strong> <code>No</code><br>
        <strong><em>Learning Rate:</em></strong> <code>1e-5</code><br>
        <strong><em>Optimizer:</em></strong> <code>SGD</code><br>
        <strong><em>Momentum:</em></strong> <code>0.9</code><br>
        <strong><em>Batch Size:</em></strong> <code>32</code><br>
        <strong><em>Regularization:</em></strong> <code>No</code><br>
        <strong><em>Input Resolution:</em></strong> <code>Low</code>
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/427d5d6c-1d5d-4448-96f6-abe4282de737" alt="Accuracy" width="300" height="200">
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/0b5592e1-0cf2-416a-9b0f-b8856e587a96" alt="Precision Recall" width="300" height="200">
      </td>
    </tr>
  </tbody>
</table>



# Image Augmentation

## Pipeline
The `augment_image` function applies the following transformations to enhance image variability:

- **Random Scaling**: Zooms in and out by up to 35%.
- **Random Resized Crop**: Crops and resizes the image to the target dimensions with a scale range of 50% to 100%.
- **Horizontal Flip**: Flips the image horizontally with a 75% probability.
- **Rotation**: Rotates the image randomly by up to 15 degrees.
- **Brightness and Contrast Adjustment**: Slightly alters brightness and contrast to simulate different lighting conditions.

| Augmentation Examples |
|------------------------|
| ![Augmentation_Example_1](https://github.com/user-attachments/assets/6b41c041-de03-49ed-90bd-669f6f268b47) |
| ![Augmentation_Example_2](https://github.com/user-attachments/assets/23e3f51c-456c-40d1-8f63-736fa1203e9b) |
| ![Augmentation_Example_3](https://github.com/user-attachments/assets/113213ea-8c5a-4039-be93-bd194d39f171) |

## Result
<table>
  <thead>
    <tr>
      <th>Model</th>
      <th>Accuracy</th>
      <th>Precision & Recall</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <strong><em>Base Model:</em></strong> <code>ResNet-50</code><br>
        <strong><em>Epochs:</em></strong> <code>100</code><br>
        <strong><em>Augmentation:</em></strong> <code>No</code><br>
        <strong><em>Learning Rate:</em></strong> <code>1e-5</code><br>
        <strong><em>Optimizer:</em></strong> <code>SGD</code><br>
        <strong><em>Momentum:</em></strong> <code>0.9</code><br>
        <strong><em>Batch Size:</em></strong> <code>32</code><br>
        <strong><em>Regularization:</em></strong> <code>No</code><br>
        <strong><em>Input Resolution:</em></strong> <code>Low</code>
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/427d5d6c-1d5d-4448-96f6-abe4282de737" alt="Accuracy" width="300" height="200">
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/0b5592e1-0cf2-416a-9b0f-b8856e587a96" alt="Precision Recall" width="300" height="200">
      </td>
    </tr>
    <tr>
      <td>
        <strong><em>Base Model:</em></strong> <code>ResNet-50</code><br>
        <strong><em>Epochs:</em></strong> <code>100</code><br>
        <strong><em>Augmentation:</em></strong> <code>Yes</code><br>
        <strong><em>Learning Rate:</em></strong> <code>1e-5</code><br>
        <strong><em>Optimizer:</em></strong> <code>SGD</code><br>
        <strong><em>Momentum:</em></strong> <code>0.9</code><br>
        <strong><em>Batch Size:</em></strong> <code>32</code><br>
        <strong><em>Regularization:</em></strong> <code>No</code><br>
        <strong><em>Input Resolution:</em></strong> <code>Medium</code>
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/504e7654-8fd3-47ce-bb94-dd293cddff0a" alt="Accuracy" width="300" height="200">
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/52b5b298-c9de-4e28-9c9b-bd676b68e3dc" alt="Precision Recall" width="300" height="200">
      </td>
    </tr>
  </tbody>
</table>

# Regularization
After applying image augmentation, the model improves but overfits, but we can address this issue by incorporating L2 regularization to enhance generalization.

## Result
<table>
  <thead>
    <tr>
      <th>Model</th>
      <th>Accuracy</th>
      <th>Precision & Recall</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <strong><em>Base Model:</em></strong> <code>ResNet-50</code><br>
        <strong><em>Epochs:</em></strong> <code>100</code><br>
        <strong><em>Augmentation:</em></strong> <code>Yes</code><br>
        <strong><em>Learning Rate:</em></strong> <code>1e-5</code><br>
        <strong><em>Optimizer:</em></strong> <code>SGD</code><br>
        <strong><em>Momentum:</em></strong> <code>0.9</code><br>
        <strong><em>Batch Size:</em></strong> <code>32</code><br>
        <strong><em>Regularization:</em></strong> <code>No</code><br>
        <strong><em>Input Resolution:</em></strong> <code>Medium</code>
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/504e7654-8fd3-47ce-bb94-dd293cddff0a" alt="Accuracy" width="300" height="200">
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/52b5b298-c9de-4e28-9c9b-bd676b68e3dc" alt="Precision Recall" width="300" height="200">
      </td>
    </tr>
    <tr>
      <td>
        <strong><em>Base Model:</em></strong> <code>ResNet-50</code><br>
        <strong><em>Epochs:</em></strong> <code>50</code><br>
        <strong><em>Augmentation:</em></strong> <code>Yes</code><br>
        <strong><em>Learning Rate:</em></strong> <code>1e-5</code><br>
        <strong><em>Optimizer:</em></strong> <code>SGD</code><br>
        <strong><em>Momentum:</em></strong> <code>0.9</code><br>
        <strong><em>Batch Size:</em></strong> <code>32</code><br>
        <strong><em>Regularization:</em></strong> <code>L2 (0.1)</code><br>
        <strong><em>Input Resolution:</em></strong> <code>Medium</code>
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/90a0f0ed-d16e-4084-aaa6-6c67601173a1" alt="Accuracy" width="300" height="200">
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/684c619d-b3e4-479f-b254-ae38fc2e6159" alt="Precision Recall" width="300" height="200">
      </td>
    </tr>
    <tr>
      <td>
        <strong><em>Base Model:</em></strong> <code>ResNet-50</code><br>
        <strong><em>Epochs:</em></strong> <code>50</code><br>
        <strong><em>Augmentation:</em></strong> <code>Yes</code><br>
        <strong><em>Learning Rate:</em></strong> <code>1e-5</code><br>
        <strong><em>Optimizer:</em></strong> <code>SGD</code><br>
        <strong><em>Momentum:</em></strong> <code>0.9</code><br>
        <strong><em>Batch Size:</em></strong> <code>32</code><br>
        <strong><em>Regularization:</em></strong> <code>L2 (0.01)</code><br>
        <strong><em>Input Resolution:</em></strong> <code>Medium</code>
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/5ae9fcff-13b1-4a9d-b1dd-88183655e541" alt="Accuracy" width="300" height="200">
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/4583520a-6798-4b9a-b0f3-7c3354060fa6" alt="Precision Recall" width="300" height="200">
      </td>
    </tr>
    <tr>
      <td>
        <strong><em>Base Model:</em></strong> <code>ResNet-50</code><br>
        <strong><em>Epochs:</em></strong> <code>50</code><br>
        <strong><em>Augmentation:</em></strong> <code>Yes</code><br>
        <strong><em>Learning Rate:</em></strong> <code>1e-5</code><br>
        <strong><em>Optimizer:</em></strong> <code>SGD</code><br>
        <strong><em>Momentum:</em></strong> <code>0.9</code><br>
        <strong><em>Batch Size:</em></strong> <code>32</code><br>
        <strong><em>Regularization:</em></strong> <code>L2 (0.05)</code><br>
        <strong><em>Input Resolution:</em></strong> <code>Medium</code>
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/9edba428-0cbc-4add-9f52-f88816df7ead" alt="Accuracy" width="300" height="200">
      </td>
      <td>
        <img src="https://github.com/user-attachments/assets/b1e1e59e-322f-4a93-b12f-f841bca99605" alt="Precision Recall" width="300" height="200">
      </td>
    </tr>
  </tbody>
</table>

# Examples
## From Train Set
![image](https://github.com/user-attachments/assets/b2216af9-8df7-44a8-be23-345b77a70431)
![image](https://github.com/user-attachments/assets/8d7e1f38-3097-4f14-bd84-ee8efb13119a)
![image](https://github.com/user-attachments/assets/6c7e3842-bc07-46d4-a0dc-e8832a143534)



## From Test Set
![image](https://github.com/user-attachments/assets/f5111891-1c5a-46a6-aa52-a9aa52f5f4f9)
![image](https://github.com/user-attachments/assets/a7bc7b11-07bf-4141-be4b-ea58240c99c5)
![image](https://github.com/user-attachments/assets/0629ce04-ac9c-49fa-9fd6-f7e18c12b0a8)



