# TraceX: A Contact Tracing App

## Project Overview
TraceX is a Salesforce-based application that enables organizations to manage contact tracing data. The project provides the necessary custom objects and metadata to set up the core contact tracing functionality within a Salesforce environment.

<p align="center">
  <img src="/screenshots/screenshots.png" alt="SS" width="800">
</p>

## Key Features
- **Custom Objects**: The application utilizes custom objects to store contact tracing data, including information about individuals and their contacts.
- **Salesforce CLI Deployment**: The project is designed to be deployed using the Salesforce CLI, allowing for easy installation and configuration in a Salesforce org.
- **Health Status Tracking**: Users can update their health status, which is automatically reflected in the application's dashboard.
- **Contact Tracing**: The app tracks and records contacts between individuals, allowing administrators to quickly identify potential exposure.
- **Permissions and Access Control**: The application includes a permission set to ensure appropriate access to the contact tracing data.

## Installation and Setup

### Install Object Schema

#### Make sure you have "git" and Salesoforce CLI installed in your system. Follow below steps to upload object schema along with permission set in your Salesforce Org.

1. Clone the `main` branch from the project repository:
   ```
   git clone --branch main https://github.com/Hi-Aman-Jain/TraceX.git
   ```
2. Open a terminal or command prompt and navigate to the cloned repository.
3. Authorize your Salesforce org:
   ```
   sfdx force:auth:web:login -a TestOrg1
   ```
4. Deploy the metadata to your Salesforce org:
   ```
   sfdx force:source:deploy -p force-app/main/default/
   ```
5. Assign the `Health_Admin` permission set to the current user:
   ```
   sfdx force:user:permset:assign -n Health_Admin
   ```
6. Open your Salesforce org and switch to the "Contact Tracing" application.

### Install Entire Application
1. Clone the `master` branch from the project repository:
   ```
   git clone --branch master https://github.com/Hi-Aman-Jain/TraceX.git
   ```
2. Open a terminal or command prompt and navigate to the cloned repository.
3. Authorize your Salesforce org:
   ```
   sfdx force:auth:web:login -a TestOrg1
   ```
4. Deploy the metadata to your Salesforce org:
   ```
   sfdx force:source:deploy -p force-app/main/default/
   ```
5. Assign the `Health_Admin` permission set to the current user:
   ```
   sfdx force:user:permset:assign -n Health_Admin
   ```
6. Open your Salesforce org and switch to the "Contact Tracing" application.

## Project Structure
The project repository contains the following key files and directories:

- `.vscode`: Contains Visual Studio Code settings.
- `config`: Holds configuration files.
- `force-app/main/default`: The main directory for the Salesforce application.
- `scripts`: Contains various script files.
- `.eslintignore`, `.forceignore`, `.gitignore`, `.prettierignore`, and `.prettierc`: Ignore files for various tools and utilities.
- `README.md`: This documentation file.

## Contribute
We welcome contributions to the TraceX project. If you find any issues or have suggestions for improvements, please feel free to open a new issue or submit a pull request.

## License
This project is licensed under the [MIT License](LICENSE).