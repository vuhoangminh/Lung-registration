# Lung-registration

## Introduction
Image registration is the process of aligning and transforming a 2D or 3D image or multiple images into a reference image. The sources of difference could be from numerous viewpoints, different sensors, times or depths. In the field of medical imaging, where images are acquired from variety of modalities, for example, X-ray scanners, MRI scanners, CT scanners, and Ultrasound scanners, image registration, is an essential tool; because it helps to combine patient data to yield additional anatomy information by finding the related spatial information.  

DIR has many exciting potential applications in diagnostic medical imaging and radiation oncology. Automated propagation of physician-drawn contours to multiple image volumes, functional imaging, and 4D dose accumulation in thoracic radiotherapy are just a few examples. However, before such applications can be successfully and safely implemented, we require that the DIR spatial accuracy performance is rigorously and objectively assessed.

In this project, we are provided four cases including intensity volumes (inhale and exhale) plus landmark points to 'train' that is to search for the optimal parameters in registration from the moving chest to the fixed one. The goals of this project are to build a robust registration method to predict 300 fixed landmarks based on provided inputs: inhale, exhale volumes and  300 moving landmarks coordinates and evaluate by 3D Euclidean distance between transformed landmarks (TRE).


## Dataset
We are given four cases. Each case includes: 

1. CaseID_300_iBH_xyz_r1.txt
2. CaseID_300_eBH_xyz_r1.txt
3. CaseID_iBHCT.img
4. CaseID_eBHCT.img

The CaseID_300_iBH_xyz_r1.txt and CaseID_300_eBH_xyz_r1.txt text files contain a list of 300 landmark locations of superior/inferior (SI) coordinate locations corresponding to
the respective iBHCT and eBHCT component phase images from a 4DCT set.  The iBHCT label represents the maximum inhale phase of the 4DCT, while the eBHCT label corresponds to the maximum exhale phase.

In the challenge, we will be given CaseID_300_eBH_xyz_r1.txt, CaseID_iBHCT.img and CaseID_eBHCT.img. Our task is to predict 
CaseID_300_iBH_xyz_r1.txt. 
