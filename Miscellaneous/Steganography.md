# Steganography Cheatsheet

Steganography is the practice of hiding secret information within non-secret data or files. This cheatsheet provides an overview of various steganography techniques and tools to assist in uncovering hidden information. **Steganography is not a part of OSCP**

## Steganography Techniques

1. **Image Steganography:**
   - Hiding data within image files.
   - Tools: zsteg, online steganography tools.

2. **File Steganography:**
   - Hiding data within other file formats such as documents, audio, or video files.
   - Tools: binwalk, exiftool.

## Steganography Tools

1. **Online Steganography Tools:**
   - Various online platforms that offer steganography decoding capabilities.
   - Examples:
     - [StegOnline](https://stegonline.georgeom.net/)
     - [CyberChef](https://gchq.github.io/CyberChef/)
     - [Aperi'Solve](https://www.aperisolve.com/)

2. **steghide:**
   - A command-line tool for hiding data within various file formats including images and audio.
   - Example usage: `steghide extract -sf <image_file>` - Extracts the hidden message inside `<image_file>`
   - Example usage: `steghide extract -sf <image_file> -p <password>` - Extracts the hidden message inside `<image_file>` with `<password>`

3. **zsteg:**
   - A command-line tool for detecting hidden data in PNG and BMP images.
   - Example usage: `zsteg <image.png>`

4. **binwalk:**
   - A command-line tool for analyzing and extracting hidden data from files.
   - Example usage: `binwalk -e <file>` - Extracts the embedded files from `<file>`

5. **exiftool:**
   - A command-line tool for reading and modifying metadata information in files, including images.
   - Example usage: `exiftool <image.jpg>`
