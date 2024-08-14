# Salesforce Lightning App Builder

## Overview
Salesforce Lightning App Builder is a powerful tool that enables users to create custom pages for Salesforce Lightning Experience and mobile apps. It offers a drag-and-drop interface to add components to a page and configure them without writing code. This flexibility allows Salesforce users to build personalized experiences that align with their business needs.

One of the challenges faced in Salesforce is displaying fields from external objects—data that resides outside the Salesforce organization—on a Salesforce record page. Since this data is external, it cannot be viewed directly on the record page without implementing certain approaches. Below are three methods to achieve this.

## Approaches to Viewing External Object Fields in Salesforce Record Pages

### 1. Custom Lightning Component
Custom Lightning Components allow you to create a tailored experience for displaying external object fields within Salesforce record pages. By using the Aura framework in the Salesforce Developer Console, a Custom Lightning Component was developed to overcome the limitation of built-in components, enabling real-time data fetching from external sources. This approach, though requiring JavaScript and Salesforce framework knowledge, offers maximum customization.

#### Apex Class File:

- CustomObject.apxc

#### Custom Lightning Component Bundle Files:

- CustomObject.cmp
- CustomObjectController.js
- CustomObjectHelper.js
- CustomObject.css
- CustomObject.auradoc
- CustomObjectRenderer.js
- CustomObject.design
- CustomObject.svg

### Setup

1. **Create the Record Page:**

   - Log in to Salesforce.
   - Navigate to the Lightning App Builder under Setup -> User Interface.
   - Create a new Record Page.
   - Add components to display fields from the custom objects.

2. **Add the Custom Lightning Component:**

   - Open the Salesforce Developer Console.
   - Create a new Lightning Component using the Aura framework.
   - Add the necessary code to display the fields from the external object.
   - Save and deploy the component.
   - Add the Custom Lightning Component to the record page in the Lightning App Builder.

### 2. Salesforce Flow Builder
When there is an external lookup relationship between an external object and a custom or standard object, Salesforce Flow Builder can be used to retrieve and display external object fields. Flow Builder offers a no-code solution, but you will need to develop the flow to automate the process of fetching and displaying external data on record pages. 

**Process Overview:**
1. **Create a New Flow:**
   - In Salesforce, navigate to Setup, then go to **Flow Builder**.
   - Click **New Flow** and select **Screen Flow** to start creating a flow that will interact with the user interface.

2. **Add a Get Records Element:**
   - Drag and drop the **Get Records** element onto the canvas.
   - Configure it to fetch the external object’s fields based on the lookup relationship with your custom or standard object.

3. **Add Screen Components:**
   - Add a **Screen** element to your flow where you can display the fetched external object data.
   - Use display components like text or rich text fields to show the external object fields retrieved by the flow.

4. **Configure the Flow on Record Page:**
   - Drag and drop the `Flow` Component onto the Record page.
   - Configure the flow to start automatically when the record page loads, or trigger it based on specific user actions.

### 3. Indirect Lookup
Indirect Lookup is a feature that allows you to link external object records with Salesforce records via an indirect lookup relationship. This method does not require additional development efforts or flow configuration. By using indirect lookups, you can view external object fields directly on Salesforce record pages as if they were native Salesforce data, simplifying the process of integrating external data.
