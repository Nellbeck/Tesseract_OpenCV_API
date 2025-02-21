# Tesseract OpenCV API

> A .NET API for extracting Machine Readable Zone (MRZ) data from images using Tesseract OCR and OpenCV.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Introduction

The **Tesseract OpenCV API** is a .NET-based project designed to extract **Machine Readable Zone (MRZ)** data from images, such as passport photos or ID cards. It leverages **Tesseract OCR** for text recognition and **OpenCV** for image preprocessing, enhancing OCR accuracy.

## Features

- **MRZ Detection & Extraction**: Identify and extract MRZ text from scanned images.
- **Image Preprocessing**: Enhance contrast, remove noise, and optimize OCR performance.
- **Fast & Efficient**: Designed to be lightweight and performant within .NET applications.
- **Easy Integration**: REST API for seamless usage in various projects.

## Installation

### Prerequisites

- Install [.NET SDK](https://dotnet.microsoft.com/download)
- Install [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) (ensure trained data files are available)
- Install [OpenCV](https://opencv.org/)

### Steps to Set Up

1. **Clone the Repository**:

   ```sh
   git clone https://github.com/Nellbeck/Tesseract_OpenCV_API.git
   cd Tesseract_OpenCV_API
   ```

2. **Restore Dependencies**:

   ```sh
   dotnet restore
   ```

3. **Build the Project**:

   ```sh
   dotnet build
   ```

## Usage

### Running the API

Start the API server:

```sh
   dotnet run
```

By default, the API runs on `http://localhost:5000`.

### API Endpoint

- ``: Accepts an image file and returns extracted MRZ data.

#### Example Request Using `curl`

```sh
curl -X POST http://localhost:5000/api/extract-mrz \
  -F 'image=@/path/to/your/image.jpg' \
  -H 'Content-Type: multipart/form-data'
```

## Configuration

Modify settings in `appsettings.json`:

```json
{
  "TesseractDataPath": "./tessdata",
  "AllowedFileExtensions": [".jpg", ".jpeg", ".png"]
}
```

## Contributing

Contributions are welcome! To contribute:

1. **Fork** the repository.
2. **Create a branch**: `git checkout -b feature/YourFeature`.
3. **Commit your changes**: `git commit -m 'Add feature'`.
4. **Push to the branch**: `git push origin feature/YourFeature`.
5. **Open a pull request**.

## License

This project is licensed under the **Apache 2.0 License**. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract)
- [OpenCV](https://opencv.org/)

