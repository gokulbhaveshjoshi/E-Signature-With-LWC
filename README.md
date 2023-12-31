# Capture Digital Signature 

To set up the LWC for collecting name and signature information, follow these three steps:

## Step 1: Configure your LWC HTML Layout
- Go to the NameAndSignature section of the LWC Sample directory on GitHub(https://github.com/forcedotcom/LWC-Mobile-Samples/tree/main/NameAndSignatureCapture).
- Copy the signaturePad component's code into your project's LWC folder.
- After copying, you can reference the component by writing `<c-signature-pad>` and configure it by setting its attributes.
## Step 2: Connect your Interface with LWC JavaScript APIs
The SignaturePad LWC provided allows you to capture data and customize the interface using JavaScript APIs and their corresponding HTML attributes.
To achieve this, invoke the API methods and connect them to the corresponding HTML attributes on the <c-signature-pad> element.
By following these steps, you can integrate the signature capture functionality into your LWC and, for example, save the signature provided by the end user for your Dreamhouse example. Below is a listing that shows the mapping between HTML attributes and JavaScript APIs:

[Listing of HTML Attribute and JavaScript API Mappings]
| Functionality                | Description                                                                                                           | HTML Attribute = “type”              | JavaScript API (Type)           |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------- | ------------------------------------ | ------------------------------- |
| Enable Name Signing          | Allows end users to type out their name, and it returns an auto-generated text-to-signature as users type their name. | enable-name-signing=”boolean”        | enableNameSigning(boolean)      |
| Enable Signature Drawing     | Allows you to prompt end users to draw their own custom signature on the provided signature pad.                      | enable-signature-drawing = “boolean” | enableSignatureDrawing(boolean) |
| Signature Stroke Thickness   | Customize the thickness of the pen stroke on the e-signature captures.                                                | stroke-thickness=”integer”           | strokeThickness(integer)        |
| Signature Pen Color          | Customize the ink color of the pen that is provided to the end user.                                                  | pen-color=”String”                   | penColor(String)                |
| Signature Pad Color          | Customize the color of the signature pad that the end user sees.                                                      | pad-color=”String”                   | padColor(String)                |
| Signature Font Color         | Customize the signature font.                                                                                         | font-color=”String”                  | font.color=String               |
| Setting an Input Field Label | Set a label for the Input field name.                                                                                 | name-input-label=”String”            | nameInputLabel=”String”         |
| Setting a Pad Label          | Set a name for the label above the signature pad.                                                                     | name-input-label=”String”            | nameInputLabel=”String”         |
| Save Signature               | Allows save an auto-generated and/or custom signature.                                                                | onclick={saveSignature}              | pad.getSignature()              |
| Clear Signature              | Allows removal of previous signature if re-do is necessary.                                                           | onclick={clearSignature}             | pad.clearSignature()            |
