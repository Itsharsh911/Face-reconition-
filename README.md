Raspberry Pi 4 Facial Recognition
This project implements a facial recognition system on a Raspberry Pi 4, utilizing a webcam for image capture and OpenCV for facial recognition. The system can train models, recognize faces, and send email notifications.

Features
- Facial Recognition: Detects and recognizes faces using Haar Cascade and a trained model.
- Headshot Capture: Capture and store headshots for training the model.
- Email Alerts: Send email notifications upon recognition events.
- Training: Train the model using a custom dataset.
- Hardware Compatibility: Works with Raspberry Pi 4 and a standard webcam.

Materials Required
- Raspberry Pi 4
- Webcam
- Python 3 (with necessary libraries installed)
- Haar Cascade file for face detection (haarcascade_frontalface_default.xml)

Directory Structure
facial_recognition_main/
├── dataset/                   # Training and testing images
├── facial_req.py              # Core script for facial recognition
├── facial_req_email.py        # Script with email notification feature
├── haarcascade_frontalface_default.xml  # Haar Cascade for face detection
├── headshots.py               # Script for capturing headshots
├── headshots_picam.py         # Headshot script for Raspberry Pi Camera
├── LICENSE                    # Licensing information
├── photo/                     # Directory for photos or screenshots
├── README.md                  # Documentation file
├── send_test_email.py         # Script to send test emails
├── train_model.py             # Script to train the facial recognition model


Setup Instructions

1.Clone the Repository
   bash
   git clone 
   cd facial_recognition_main
   ```

2. Install Dependencies
   bash
   pip install -r requirements.txt
  
   Ensure OpenCV, NumPy, and necessary email libraries are installed.

3. Prepare the Dataset
   - Place training images in the dataset/ directory.
   - Organize images by folders named after individuals (e.g., dataset/Person1/).

4. Train the Model
   bash
   python train_model.py
  

5. Run Facial Recognition
   bash
   python facial_req.py
  

6. Enable Email Alerts(optional):
   - Configure email settings in facial_req_email.py.
   - Run the email-enabled script:
     bash
     python facial_req_email.py
     

Usag
Capture Headshots  To capture headshots for training:
bash
python headshots.py
For Raspberry Pi Camera:
bash
python headshots_picam.py

Send Test Email
To verify email configuration:
bash
python send_test_email.py

Example Output
When the script detects a face, it:
- Identifies the individual (if trained)
- Logs the event
- Optionally sends an email notification with a photo attachment
