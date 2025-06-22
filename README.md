# Document scanner with ML Kit on .NET for Android [![Nuget](https://img.shields.io/nuget/v/MLKitDocumentScanner)](https://www.nuget.org/packages/Xamarin.Google.MLKit.DocumentScanner)
[Learn more about ML Kit document scanner](https://developers.google.com/ml-kit/vision/doc-scanner) | [Official docs](https://developers.google.com/ml-kit/vision/doc-scanner/android)

Digitizing physical documents, which allows users to convert physical documents into digital formats has become a very common user journey in mobile apps. ML Kit's document scanner API provides a comprehensive solution with a high-quality, consistent UI flow across Android apps and devices. Once the document scanner flow is triggered from your app, users retain full control over the scanning process. They can optionally crop the scanned documents, apply filters, remove shadows or stains, and easily send the digitized files back to your app.

The UI flow, ML models and other large resources are delivered using Google Play services, which means:

- Low binary size impact (all ML models and large resources are downloaded centrally in Google Play services).
- No camera permission is required - the document scanner leverages the Google Play services' camera permission, and users are in control of which files to share back with your app.

The entire document scanner flow operates on-device.

## Key capabilities
- High-quality and consistent user interface for digitizing physical documents.
- Automatic capture with document detection.
- Accurate edge detection for optimal crop results.
- Automatic rotation detection to show documents upright.
- Editing functionalities to crop, apply filters, remove shadows, clean stains, and seamlessly send digitized files back to your app.
- On-device processing, preserving user's privacy.
- No camera permission is needed from your app.
- Low apk binary size impact.

## Customization
The document scanner API provides a high-quality fully fledged UI flow that is consistent across Android apps. However, there is also room to customize some aspects of the user experience:

- Maximum number of pages:
Set a limit to the number of pages scanned.

- Gallery import:
Enable or disable the capability to import from the photo gallery.

- Editing functionalities:
Customize the editing functionalities available to the user by choosing from 3 modes:

	* SCANNER_MODE_BASE: basic editing capabilities (crop, rotate, reorder pages, etc…).
	* SCANNER_MODE_BASE_WITH_FILTER: adds image filters (grayscale, auto image enhancement, etc…) to the SCANNER_MODE_BASE mode.
	* SCANNER_MODE_FULL (default): adds ML-enabled image cleaning capabilities (erase stains, fingers, etc…) to the SCANNER_MODE_BASE_WITH_FILTER mode. This mode will also allow future major features to be automatically added along with Google Play services updates, while the other two modes will maintain their current feature sets and only receive minor refinements.