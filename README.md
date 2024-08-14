
# Salesforce Lightning App Builder

## Overview
Salesforce Lightning App Builder is a powerful tool that enables users to create custom pages for Salesforce Lightning Experience and mobile apps. It offers a drag-and-drop interface to add components to a page and configure them without writing code. This flexibility allows Salesforce users to build personalized experiences that align with their business needs.

One of the challenges faced in Salesforce is displaying fields from external objects—data that resides outside the Salesforce organization—on a Salesforce record page. Since this data is external, it cannot be viewed directly on the record page without implementing certain approaches. Below are three methods to achieve this.

## Approaches to Viewing External Object Fields in Salesforce Record Pages

### 1. Custom Lightning Component
Custom Lightning Components allow you to create a tailored experience for displaying external object fields within Salesforce record pages. By leveraging Salesforce’s Lightning Web Components (LWC) or Aura Components, you can fetch and display data from external sources in real-time. This approach requires knowledge of JavaScript and Salesforce’s component framework, but it offers the highest level of customization.

### 2. Salesforce Flow Builder
When there is an external lookup relationship between the external object and a custom or standard object, Salesforce Flow Builder can be used to retrieve and display external object fields. Flow Builder provides a no-code solution where you can create automated processes that fetch external data and present it on record pages. This method is ideal for those who prefer a point-and-click interface without writing code.

### 3. Indirect Lookup
Indirect Lookup is a feature that allows you to link external object records with Salesforce records via an indirect lookup relationship. This method does not require additional development efforts or flow configuration. By using indirect lookups, you can view external object fields directly on Salesforce record pages as if they were native Salesforce data, simplifying the process of integrating external data.

# Salesforce Lightning App Builder 2

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
