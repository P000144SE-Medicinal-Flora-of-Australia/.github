# 🌿 Customary Medicinal Flora of Australia (CMFoA)

<div align="center">

[![AWS](https://img.shields.io/badge/AWS-Cloud%20Hosted-orange?style=for-the-badge&logo=amazon-aws)](https://cmfoa.info)
[![React](https://img.shields.io/badge/React-Frontend-blue?style=for-the-badge&logo=react)](https://reactjs.org/)
[![Python](https://img.shields.io/badge/Python-Backend-green?style=for-the-badge&logo=python)](https://python.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

**Bridging Indigenous Knowledge and Modern Cheminformatics**

[🌐 Visit Platform](https://cmfoa.info) • [📖 Documentation](docs/) • [🔬 Research Paper](paper/)

</div>

---

## 🛠️ Technology Stack

<div align="center">

| Frontend | Backend | Cloud | AI/ML |
|----------|---------|-------|-------|
| ![React](https://img.shields.io/badge/-React-61dafb?style=flat-square&logo=react&logoColor=white) | ![Python](https://img.shields.io/badge/-Python-3776ab?style=flat-square&logo=python&logoColor=white) | ![AWS](https://img.shields.io/badge/-AWS-ff9900?style=flat-square&logo=amazon-aws&logoColor=white) | ![Claude](https://img.shields.io/badge/-Claude%203.5-ff6b35?style=flat-square) |
| ![Node.js](https://img.shields.io/badge/-Node.js-339933?style=flat-square&logo=node.js&logoColor=white) | ![Flask](https://img.shields.io/badge/-Flask-000000?style=flat-square&logo=flask&logoColor=white) | ![DynamoDB](https://img.shields.io/badge/-DynamoDB-4053d6?style=flat-square&logo=amazon-dynamodb&logoColor=white) | ![RAG](https://img.shields.io/badge/-RAG-purple?style=flat-square) |
| ![JavaScript](https://img.shields.io/badge/-JavaScript-f7df1e?style=flat-square&logo=javascript&logoColor=black) | ![Lambda](https://img.shields.io/badge/-Lambda-ff9900?style=flat-square&logo=aws-lambda&logoColor=white) | ![S3](https://img.shields.io/badge/-S3-569a31?style=flat-square&logo=amazon-s3&logoColor=white) | ![Bedrock](https://img.shields.io/badge/-Bedrock-ff9900?style=flat-square) |

</div>

---

## 📊 Dataset Overview

| Component | Count | Description |
|-----------|-------|-------------|
| **Plant Genera** | 266 | Australian flora with documented customary use |
| **Chemical Classes** | 132 | Specialized metabolite classifications |
| **Therapeutic Categories** | 27 | Traditional medicinal applications |
| **Chemical Entities (v2)** | 5,821 | Detailed molecular structures with SMILES |

<div align="center">

### 📥 Download Dataset Metadata

<button onclick="downloadMetadata()" style="
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  border: none;
  padding: 12px 24px;
  border-radius: 8px;
  font-size: 16px;
  font-weight: bold;
  cursor: pointer;
  box-shadow: 0 4px 15px rgba(0,0,0,0.2);
  transition: all 0.3s ease;
" onmouseover="this.style.transform='translateY(-2px)'; this.style.boxShadow='0 6px 20px rgba(0,0,0,0.3)'" onmouseout="this.style.transform='translateY(0px)'; this.style.boxShadow='0 4px 15px rgba(0,0,0,0.2)'">
  📊 Download Metadata CSV
</button>

<script>
function downloadMetadata() {
  const metadata = [
    ['Component', 'Count', 'Description', 'Data_Type', 'Source', 'Last_Updated'],
    ['Plant Genera', '266', 'Australian flora with documented customary use', 'Taxonomic', 'Manual Curation + CSIRO', '2024-01-15'],
    ['Chemical Classes', '132', 'Specialized metabolite classifications', 'Chemical', 'Literature Review', '2024-01-15'],
    ['Therapeutic Categories', '27', 'Traditional medicinal applications', 'Ethnobotanical', 'Indigenous Knowledge', '2024-01-15'],
    ['Chemical Entities (v2)', '5821', 'Detailed molecular structures with SMILES', 'Molecular', 'CSIRO Dataset', '2024-02-01'],
    ['SMILES Codes', '5821', 'Simplified molecular input line entry system', 'Chemical_Identifier', 'Automated', '2024-02-01'],
    ['Taxonomic IDs', '266', 'Standardized botanical identifiers', 'Taxonomic_Identifier', 'GBIF/APNI', '2024-01-15'],
    ['Literature References', '450+', 'Peer-reviewed publications', 'Bibliographic', 'SciFindern/PubMed', '2024-01-15'],
    ['Geographic Distribution', '266', 'Australian bioregions and states', 'Geospatial', 'CSIRO/GBIF', '2024-01-15']
  ];
  
  const csvContent = metadata.map(row => row.map(field => `"${field}"`).join(',')).join('\n');
  const blob = new Blob([csvContent], { type: 'text/csv;charset=utf-8;' });
  const link = document.createElement('a');
  
  if (link.download !== undefined) {
    const url = URL.createObjectURL(blob);
    link.setAttribute('href', url);
    link.setAttribute('download', 'cmfoa_metadata.csv');
    link.style.visibility = 'hidden';
    document.body.appendChild(link);
    link.click();
    document.body.removeChild(link);
  }
}
</script>

</div>

## 🚀 Quick Start

### Prerequisites
- Node.js 16+
- Python 3.8+
- AWS CLI configured
- Git

### Local Development

```bash
# Clone the repository
git clone https://github.com/P000144SE-Medicinal-Flora-of-Australia/cmfoa-platform.git
cd cmfoa-platform

# Install frontend dependencies
npm install

# Install backend dependencies
pip install -r requirements.txt

# Start development server
npm run dev
```

### Cloud Deployment

```bash
# Deploy to AWS
amplify init
amplify push
```

## 🔬 Research Impact

> *"This platform provides an entry-point for the public to engage with the data through the AI assistant interface, which lowers the conceptual barrier through a familiar natural-language environment, as well as affording a functional resource for the academic community."*

### Publications
- **Specialised Metabolites of Australia's Customary Medicinal Flora** - CSIRO Publishing (2025)
- **Developing cheminformatics platforms: implementation of a cloud-hosted natural product repository** - [Journal] (2024)


---

## 🏆 Acknowledgments

- **RMIT RACE Hub** - AWS infrastructure and technical support
- **CSIRO** - Australian Natural Products dataset
- **Aboriginal and Torres Strait Islander Knowledge Holders** - Traditional medicinal knowledge
- **Monash University** - Foundational research by David Collins and Don McGilvery

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](../LICENSE) file for details.

## 📞 Contact

- **Technical Support**: [RACE Hub](mailto:race@rmit.edu.au)
- **Platform**: [cmfoa.info](https://cmfoa.info)
