# Voice-Based-Virtual-Trial-Room

The project takes in voice input from the user and retrieves the most relevant clothing items from its database and overlays it on the image of the user. Our target was to create an automated virtual try on operated through voice.

Our model aims at generating photo-realistic try-on result while preserving both the character of clothes and details of human identity (posture, body parts, bottom clothes) through speech input from the user. This has the potential to revolutionize user’s experience while shopping for clothes online.

## Voice to Text

We make use of Wav2Vec model for generating transcript for the user’s voice input.

![alt text](https://github.com/banerjeepragyan/Voice-Based-Virtual-Trial-Room/blob/main/models/wav2vec2.png)

## Cloth Selection

● We employ CLIP Encoders to generate embeddings for clothes and user’s cloth description.

● Most similar cloth is selected using cosine similarity between Image embeddings and text embedding.

![alt text](https://github.com/banerjeepragyan/Voice-Based-Virtual-Trial-Room/blob/main/models/clip.png)

## Overlaying Cloth Image

We overlay the cloth image using 3 modules involving

○ Semantic Generation Module (SGM),

○ Clothes Warping Module (CWM)

○ Content Fusion Module (CFM).

![alt text](https://github.com/banerjeepragyan/Voice-Based-Virtual-Trial-Room/blob/main/models/acgpn.png)

## Results

The following are some of the results we achieved 

![alt text](https://github.com/banerjeepragyan/Voice-Based-Virtual-Trial-Room/blob/main/results.png)

## References

● Wav2Vec2 : [Unsupervised pre-training for speech recognition](https://arxiv.org/pdf/2006.11477.pdf)

● CLIP: [Learning Transferable Visual Models From Natural Language Supervision](https://arxiv.org/pdf/2103.00020.pdf)

● Towards [Photo-Realistic Virtual Try-On by Adaptively Generating↔Preserving Image Content](https://arxiv.org/pdf/2003.05863.pdf)
