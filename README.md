# navigateToRecord Aura Component

This Aura component is designed for Salesforce and is capable of redirecting users to a specific Salesforce record once a Flow involving this component completes. It's implemented to be used primarily in Salesforce Lightning Flows as a final action that takes users directly to a designated record. This is helpful particularly in the Salesforce mobile as url redirects won't work there.

## Features

-  **Lightning Quick Action**: The component can be configured to act as a quick action.
-  **Flow Integration**: Suitable for use in Salesforce Flows, especially at the end of the Flow to redirect users.
-  **Customizable**: Through the `recordId` attribute, users can specify which record to navigate after the Flow execution.

## Prerequisites

Before you start using `navigateToRecord`, make sure you have:
-  Access to a Salesforce org (Developer, Enterprise, or Unlimited edition).
-  Permission to edit and deploy Aura Components and Flows.
-  Salesforce CLI installed, if you intend to deploy the component via command line.
-  Visual Studio Code with Salesforce DX for local development.

## Installation

To deploy this Aura component to your Salesforce organization, follow the steps below:

1. **Clone the Repository**
   ```sh
   git clone https://github.com/normcopeland/navigateToRecord.git
   cd navigateToRecord
   ```

2. **Deploy to Salesforce**
   Use Salesforce CLI to deploy the component:
   ```sh
   sfdx force:source:deploy -p force-app/main/default/aura/navigateToRecord/ -u YourOrgAlias
   ```
   Replace `YourOrgAlias` with your Salesforce org alias.

## Usage

Once deployed, you can incorporate `navigateToRecord` into your Salesforce Flows by adding it as a Core Action in Flow Builder. Be sure to pass the `recordId` dynamically to the component based on the context of the Flow.

## Component Structure

This component bundle includes the following files:
-  **navigateToRecord.cmp**: Main component markup.
-  **navigateToRecordController.js**: Client-side controller.
-  **navigateToRecord.design**: Design configuration for use in Flow Builder.
-  **navigateToRecord.cmp-meta.xml**: Metadata configuration file for deployment settings.