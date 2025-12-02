# Azure Content Understanding

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Azure](https://img.shields.io/badge/Azure-Content%20Understanding-0078D4.svg)](https://learn.microsoft.com/azure/ai-services/content-understanding/)

A collection of Jupyter notebooks demonstrating the capabilities of **Azure Content Understanding** (GA version - API 2025-11-01). These demos showcase how to process and analyze documents, images, videos, and audio files using generative AI to extract structured data from unstructured content.

<img src="https://camo.githubusercontent.com/b6d5938c6519dbec92e6972598843f7a0ab548a567b38e4ab5d2ca34d07706b7/68747470733a2f2f6c6561726e2e6d6963726f736f66742e636f6d2f656e2d75732f617a7572652f61692d73657276696365732f636f6e74656e742d756e6465727374616e64696e672f6d656469612f6f766572766965772f636f6e74656e742d756e6465727374616e64696e672d6672616d65776f726b2d323032352e706e67236c69676874626f78">

## 🎯 Overview

Azure Content Understanding is a Generally Available (GA) Azure AI service that uses generative AI to transform unstructured content into structured, searchable data. This repository contains practical, ready-to-run notebooks that demonstrate various capabilities of the service across different content types.

## 🔍 What is Azure Content Understanding?

Azure Content Understanding in Foundry Tools is an AI service available as part of the Microsoft Foundry Resource in Azure. It processes and ingests content of many types:

- **Documents** (PDF, DOCX, XLSX, images)
- **Videos** (MP4, MOV, AVI)
- **Audio** (WAV, MP3, M4A)
- **Images** (JPG, PNG, TIFF)

The service offers a streamlined process to reason over large amounts of unstructured data, accelerating time-to-value by generating structured output that can be integrated into automation and analytical workflows.

## ✨ Key Features

### Content Extraction
- **Document Processing**: OCR, layout analysis, table recognition, and structural element detection
- **Video Analysis**: Frame extraction, shot detection, speech-to-text transcription
- **Audio Processing**: Speech-to-text transcription with high accuracy
- **Image Analysis**: Visual content understanding and data extraction

### Generative Capabilities
- **Field Extraction**: Define custom schemas to extract specific fields from any content type
- **Classification**: Categorize content into up to 200 categories with integrated classification
- **Content Summarization**: Generate summaries and insights from extracted content
- **Face Description**: Generate textual descriptions of faces in video and image content (with proper authorization)

### Enterprise Features (GA)
- Microsoft Entra ID authentication
- Managed identities support
- Customer-managed keys
- Virtual networks and private endpoints
- Transparent pricing model
- Model deployment flexibility (GPT-4o, GPT-4o-mini)

## 📚 Python Notebooks

<table>
  <thead>
    <tr>
      <th>Notebook</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="1.%20Managing%20%20analyzers.ipynb">Managing analyzers</a></td>
      <td>Learn how to create, configure, and manage analyzers for different content types.</td>
    </tr>
    <tr>
      <td><a href="2.%20Field%20extraction.ipynb">Field extraction</a></td>
      <td>Demonstrates extracting predefined fields from documents using built-in schemas.</td>
    </tr>
    <tr>
      <td><a href="3.%20Custom%20field%20extraction.ipynb">Custom field extraction</a></td>
      <td>Shows how to define and extract custom fields tailored to your business needs.</td>
    </tr>
    <tr>
      <td><a href="4.%20Classifier.ipynb">Classifier</a></td>
      <td>Explains how to classify content into categories using integrated classification APIs.</td>
    </tr>
    <tr>
      <td><a href="5.%20Document%20content%20extraction.ipynb">Document content extraction</a></td>
      <td>Focuses on OCR, layout analysis, and table recognition for multi-page documents.</td>
    </tr>
    <tr>
      <td><a href="6.%20Audio%20extraction.ipynb">Audio extraction</a></td>
      <td>Covers speech-to-text transcription and audio content analysis with speaker identification.</td>
    </tr>
    <tr>
      <td><a href="7.%20Video%20content%20extraction.ipynb">Video content extraction</a></td>
      <td>Demonstrates video frame extraction, scene detection, and speech transcription from video.</td>
    </tr>
  </tbody>
</table>

## 📦 Prerequisites

Before running these notebooks, ensure you have:

1. **Azure Subscription**
   - An active Azure subscription ([Create one for free](https://azure.microsoft.com/free/))

2. **Azure AI Foundry Resource**
   - Create an [Azure AI Foundry resource](https://portal.azure.com/#create/Microsoft.CognitiveServicesAIFoundry)
   - Note your endpoint URL and API key

3. **Model Deployments** (Required for prebuilt analyzers)
   - Deploy GPT-4.1-mini, GPT-4.1 model
   - Deploy text-embedding-3-large model
   - See [deployment documentation](https://learn.microsoft.com/azure/ai-foundry/foundry-models/concepts/deployment-types)

4. **Role Assignment**
   - Grant yourself the **Cognitive Services User** role on the resource
   - This is required even if you're the resource owner

5. **Python Environment**
   - Python 3.8 or higher
   - Jupyter Notebook or JupyterLab

## 📓 Notebooks Overview

This repository contains demonstration notebooks covering:

### Document Analysis
- Document field extraction with custom schemas
- Layout analysis and table extraction
- Multi-page document processing
- Classification and routing

### Image Processing
- Image content extraction
- Visual question answering
- Figure detection and analysis
- Object and text recognition

### Video Analysis
- Video frame extraction
- Scene detection and segmentation
- Speech transcription from video
- Visual content summarization

### Audio Processing
- Audio transcription
- Speaker identification
- Audio content analysis

### Advanced Scenarios
- Multi-modal content analysis
- RAG (Retrieval-Augmented Generation) integration
- Batch processing workflows
- Custom analyzer creation

## 💼 Use Cases

Azure Content Understanding is ideal for:

- **Financial Services**: Tax document processing, mortgage application analysis
- **Healthcare**: Medical record extraction and analysis
- **Legal**: Contract review and clause extraction
- **Manufacturing**: Quality control and defect detection
- **Retail**: Inventory management and shelf analysis
- **Media**: Content cataloging and metadata extraction
- **Analytics & Reporting**: Enhanced business intelligence from unstructured data

## 📌 API Version

These notebooks use the **GA API version: `2025-11-01`**

This is the Generally Available version with production-ready features, enterprise security, and enhanced capabilities compared to previous preview versions.

### Migration from Preview
If you're migrating from preview API versions (`2024-12-01-preview` or `2025-05-01-preview`), refer to the [migration guide](https://learn.microsoft.com/azure/ai-services/content-understanding/how-to/migration-preview-to-ga).

### Breaking Changes from Preview
- Managed capacity for preview models retired (BYO model deployments required)
- Dedicated classifier APIs deprecated (now integrated in analyzer API)
- Video segmentation unified with classification capabilities

## 📚 Resources

### Official Documentation
- [Azure Content Understanding Overview](https://learn.microsoft.com/azure/ai-services/content-understanding/overview)
- [What's New in Content Understanding](https://learn.microsoft.com/azure/ai-services/content-understanding/whats-new)
- [Content Understanding Studio](https://aka.ms/cu-studio)
- [Pricing Information](https://learn.microsoft.com/azure/ai-services/content-understanding/pricing-explainer)
- [Language and Region Support](https://learn.microsoft.com/azure/ai-services/content-understanding/language-region-support)

### Related Repositories
- [Official Python Samples](https://github.com/Azure-Samples/azure-ai-content-understanding-python)
- [Official .NET Samples](https://github.com/Azure-Samples/azure-ai-content-understanding-dotnet)

### Additional Resources
- [Responsible AI Guidelines](https://learn.microsoft.com/azure/ai-foundry/responsible-ai/content-understanding/transparency-note)
- [Azure AI Foundry Documentation](https://learn.microsoft.com/azure/ai-foundry/)

## 👤 Author

**Serge Retkowsky**
- GitHub: [@retkowsky](https://github.com/retkowsky)
- LinkedIn: [serger](https://www.linkedin.com/in/serger/)
- YouTube: [@serge1840](https://www.youtube.com/@serge1840/videos)
- Medium: [@sergems18](https://medium.com/@sergems18)
- Role: AI Global Black Belt @ Microsoft France

**Last Updated**: 02-December-2025

For questions, issues, or feedback, please open an issue in this repository or contact through the channels above.


