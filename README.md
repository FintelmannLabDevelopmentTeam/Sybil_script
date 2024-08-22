# Sybil_script
This respository contains a Bash script for running Sybil on a single LDCT.


In the sybil_run.txt file, fill http://localhost:[PORT]/dicom/files with your chosen
port. Next, with the extracted folder “sybil_demo_data/” in the same working
directory, you can run the demo using the sybil_run.txt file:
sh sybil_run.txt
The curl command may need to be installed with your package manager depending
on your OS.
Given that LDCTs usually are usually composed of dozens of DICOM images, we
provide this text file that allows you to loop over all the images in a directory
(example: sybil_demo_data or any other directory containing the images for a
single patient) and send them to the API as one single request.
Be sure to replace [PORT] in the sybil_run.txt file with your chosen port number.
Important Note: Each request to this endpoint should be the equivalent of a
single exam.
4. After a few minutes, you will receive a JSON response like so:

{
  "data": {
    "predictions": [
      [
        [
          0. 021628819563619374,
          0. 03857256315036462,
          0. 07191945816622261,
          0.07926975188037134,
          0. 09584583525781108,
          0.13568094038444453
        ]
      ]
    ]
  ｝
  "message": null,
  "metadata": null,
  "runtime": "83.05s",
  "statusCode":
  200
}
