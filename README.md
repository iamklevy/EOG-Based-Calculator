# EOG-Based-Calculator

This project involves developing a human-computer interface (HCI) based on electrooculography (EOG) signals to create a simple calculator. The system simulates user's input of numbers and performing basic arithmetic operations through eye movements.

Note: simulation app on the master branch

![Screenshot (179)](https://github.com/iamklevy/EOG-Based-Calculator/assets/94145850/e1bab884-c2c2-44e1-ad85-3cb5e2f56f96)

### Runtime Demo 
# red for hover, pink for selection
<p>
    <video src="https://github.com/user-attachments/assets/d7559b27-54ab-4a20-90b2-ae11b8cc0299" />
      *Your display does not support the video tag. Open a browser to see the video.*
  </p>
      
#### 1. Data Acquisition
The dataset that is included in this branch is turkish and it's probably the only open-source one available for EOG signals, it includes raw EOG signals captured during various eye movements corresponding to different calculator operations (digits 0-9, operations +, -, x, /, and control commands like C for clear and E for exist).

#### 2. EOG Preprocessing
EOG data often contains noise and artifacts that need to be filtered out. Preprocessing steps include:
- **Noise Filtering:** Using filters (e.g., band-pass filters) to remove high-frequency noise and baseline drift.
- **Artifact Removal:** Techniques like Independent Component Analysis (ICA) or regression methods are used to eliminate artifacts from blinking and other muscular activities.

#### 3. Feature Extraction
Two approaches for feature extraction will be compared:
- **Raw Samples:** Directly using raw EOG signal samples as features.
- **Wavelet Coefficients:** Applying wavelet transform to decompose EOG signals into different frequency bands, then using coefficients from the EOG band as features.

#### 4. Classification
A classifier is chosen (e.g., Support Vector Machine, Random Forest, or Neural Network). The classifier will be trained and tested with different parameter settings to achieve the best results for each class (digits and operations).
- **Parameter Tuning:** Techniques like grid search or random search will be used to find the optimal parameters for the chosen classifier.

#### 5. Feature Comparison
The performance of the classifier using raw samples and wavelet coefficients will be compared based on the achieved accuracy. This comparison will help determine the most effective feature extraction method for EOG signals in this application.

#### 6. User Interface
A simple calculator interface is developed with the following features:
- **Digits and Operations:** Buttons for digits (0-9) and operations (+, -, x, /).
- **Control Buttons:** 'C' for clear and 'E' for exit.
- **User Interaction:** The interface will be designed to require minimal movements. Each choice (digit, operation, digit) should be achievable with only two eye movements and a blink to select.
- **Display:** The user's choices will be displayed on the screen in a text box. The result will appear automatically after selecting the second digit.
- **Layout:** Buttons will be arranged to facilitate easy selection using eye movements.

#### Simulation Workflow
1. **Data Collection:** Obtain EOG data corresponding to different eye movements.
2. **Preprocessing:** Clean the EOG signals to remove noise and artifacts.
3. **Feature Extraction:** Extract features using raw samples and wavelet coefficients.
4. **Training and Testing:** Train the classifier on the extracted features and test with different parameters to find the best configuration.
5. **Feature Comparison:** Compare the performance of raw samples and wavelet coefficients.
6. **UI Development:** A simple calculator interface that allows input through eye movements.
7. **Testing:** Evaluate the overall system performance and usability.

This project will demonstrate the feasibility of using EOG signals for a practical application, providing insights into signal processing, feature extraction, and classification techniques in the context of human-computer interaction.
