
# ImageUtilities

Use the Image Utilities integration to perform various image processing and manipulation tasks within your playbook workflows. Important: This integration requires a Remote Agent configured with the tesseract-ocr and playwright packages to function correctly.

Python Version - V3_11


#### Dependencies
| |
|-|
|google_api_python_client-2.187.0-py3-none-any.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|google_auth_httplib2-0.2.1-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|google_auth-2.43.0-py2.py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|pillow-12.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|certifi-2025.11.12-py3-none-any.whl|
|pyparsing-3.2.5-py3-none-any.whl|
|urllib3-2.5.0-py3-none-any.whl|
|httplib2-0.31.0-py3-none-any.whl|
|google_api_core-2.28.1-py3-none-any.whl|
|protobuf-6.33.1-py3-none-any.whl|
|cachetools-6.2.2-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|pytesseract-0.3.13-py3-none-any.whl|
|anyio-4.12.0-py3-none-any.whl|
|greenlet-3.2.4-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|pdf2image-1.17.0-py3-none-any.whl|
|packaging-25.0-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|TIPCommon-2.2.15-py2.py3-none-any.whl|
|charset_normalizer-3.4.4-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|googleapis_common_protos-1.72.0-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|idna-3.11-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|pyee-13.0.0-py3-none-any.whl|
|playwright-1.56.0-py3-none-manylinux1_x86_64.whl|


## Actions
#### OCR Image
Use the OCR Image action to perform optical character recognition (OCR) and extract text from an image file. Important: This action requires a Remote Agent with the tesseract-ocr package installed to function correctly.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Base64 Encoded Image|The base64 encoded string of the image file.|False|String||
|File Path|The path to the image file. If both "Base64 Encoded Image" and "File Path" are provided, "Base64 Encoded Image" is processed.|False|String||



##### JSON Results
```json
{"extracted_text": "abc"}
```



#### Rasterize Content
Use the Rasterize Content action to convert vector or complex content into a fixed, bitmap image format. Important: This action requires a Remote Agent to function correctly.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Input Type|The type of content that the action uses as its primary input.|True|List|HTML|
|URLs or Body|The input content to be rasterized, based on the selected Input Type. If URL is selected, provide a comma-separated list of URLs. If Email or HTML is selected, provide the full content body of that respective input.|True|String|None|
|Output Type|The resulting output format for the rasterized content.|False|List|PNG|
|Export Method|The method used to output the generated content.|False|List|Case Attachment|
|Width|The width (in pixels) used for the generated raster content.|True|String|1920|
|Height|The height (in pixels) used for the generated raster content.|True|String|1080|
|Full Screen|If selected, the content is rendered across the entire browser window before being rasterized.|False|Boolean|false|
|Timeout|The maximum time (in seconds) the browser dedicates to rendering the content before rasterization begins. Max: 120|False|String|120|
|Wait For|The specific state the browser must reach before the action proceeds with rasterization or content extraction. The NETWORK_IDLE state is generally the most reliable.|False|List|NETWORK_IDLE|
|Wait for Selector|A CSS selector that the action waits for to appear on the page before capturing the screenshot. This setting is highly recommended for pages where content loads dynamically, as it ensures all elements are present before the action executes.|False|String|None|



##### JSON Results
```json
[{"attachment_name": "", "file_path": ""}]
```



#### Convert File
Use the Convert File action to change the format of a specified file. Important: This action requires a Remote Agent to function correctly.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Input File Format|The original format of the file that the action converts.|True|List|PNG|
|Input File Path|The path to the file that the action converts.|True|String|None|
|Output File Format|The resulting format of the file after the conversion process.|True|List|PDF|



##### JSON Results
```json
[{"output_format": "", "file_path": ""}]
```



#### Ping
Use the Ping action to test the connectivity to Image Utilities.
Timeout - 600 Seconds



##### JSON Results
```json
{}
```









