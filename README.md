# odata-v2-salesforce-api
Integrate Salesforce with an OData service using OData 2.0. This setup enables querying and manipulating Salesforce data in a standardized manner, facilitating efficient data exchange and interoperability between Salesforce and other systems that support OData 2.0.


# Salesforce Lightning App Builder

## Overview

The project also includes a Salesforce Lightning App Builder configuration to view fields from custom objects and external objects on a record page. This enables a consolidated view of data directly within Salesforce.

## Project Structure

The project is organized into the following main components:

### 1. Record Page Configuration

The record page is set up to display fields from the custom objects and the external object using built-in components from the record page component palette. The record page can be found under `Setup` -> `User Interface` -> `Lightning App Builder`.

### 2. Custom Lightning Component

To overcome the limitation of the built-in components not displaying external object fields, a Custom Lightning Component was created using the Aura framework in the Salesforce Developer Console.

#### Apex Class File:

- `CustomObject.apxc`

#### Custom Lightning Component Bundle Files:

- `CustomObject.cmp`
- `CustomObjectController.js`
- `CustomObjectHelper.js`
- `CustomObject.css`
- `CustomObject.auradoc`
- `CustomObjectRenderer.js`
- `CustomObject.design`
- `CustomObject.svg`

### Setup

1. **Create the Record Page:**

   - Log in to Salesforce.
   - Navigate to the Lightning App Builder under `Setup` -> `User Interface`.
   - Create a new Record Page.
   - Add components to display fields from the custom objects.

2. **Add the Custom Lightning Component:**

   - Open the Salesforce Developer Console.
   - Create a new Lightning Component using the Aura framework.
   - Add the necessary code to display the fields from the external object.
   - Save and deploy the component.
   - Add the Custom Lightning Component to the record page in the Lightning App Builder.
