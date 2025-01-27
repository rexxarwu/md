
# FA Agent for Annual Report Writing

## Project Introduction
The "FA Agent for Annual Report Writing" project aims to automate the creation of comprehensive annual reports. The project applies the multi-agent technique to streamline the data retrieval, analysis, and report generation process, which ensures consistent, efficient, and high-quality reports for organizational use.

---

## Project Goals
1. Automate the extraction of relevant financial and operational data.
2. Streamline the analysis process using predefined AI models and tools.
3. Generate structured and comprehensive annual reports with minimal human intervention.

---

## Project Steps

### Environment Setup
- **Setup Instructions**: Install the library: pyautogen, finrobot, sec-api and all the dependencies.
- **Commands or Tools to Install and Activate**:
  - pip in Python environment.
  - "!pip install {lib}" in colab for cloud-based execution.

### Framework Configuration
- **Agent Registration**:
  - **Agent 1**: user proxy to execute python functions and control the conversations.
  - **Agent 2**: expert agent who is proficient in financial analytical writing.
  - **Agent 3**: shadow/inner-assistant to handle isolated long-context Q&As.  (The inner-assistant helps to hide the large files contents obtained and leave the user interface clean. It can communicate with the expert agent to handle long-context prompts.)
- **API Key Configuration**:
  - OpenAI API keys for analysis (limited and paid). Here we create an environment file and set the OpenAI API key in it.
  - Sec_api & FMP_api which are free. (sec-api.io & site.financialmodelingprep.com/developer/docs)

### Data Retrieval
- Connect to fmp-api and sec-api that provides real stock data and reports.
- Use fmp tools FMPUtils.get_sec_report to retrieve the annual report.

### Data Analysis
- Given the report analysis tool in finrobot, use the expert agent to analyze the obtained data from given report.
- Perform calculations and identify trends using statistical methods. (Done by the expert agent)
- Generate visualizations to provide direct comparisons that support analysis.

### Report Generation
- Format the analyzed data into different sections for more specific analysis.
- Give clear instructions on the sections that the report should include to let the agent generate corresponding report.
- Export the report in desired pdf format given "ReportLabUtils.build_annual_report" function.

### Testing and Validation
- Validate data retrieval outputs against source records.
- Test the functions applied to ensure the outputs are desired. Note: the register_toolkit function returns str type, which might not meet the requirment of return type.
- Review generated reports for alignment with organizational standards.

---

## Notes
1. Ensure API keys are securely stored and rotated periodically to maintain security.
2. The functions used are still in active updates, so that modifications would be necessary to keep up with the new function definitions.
3. Include detailed documentation to facilitate maintenance and scalability.

---

## References
1. *Gen101*, (https://citrine-music-bce.notion.site/GenAI-101-129ebcc111348119b72cf397bd7a83a3)
2. *Free Stock Market API and Financial Statements API*, (https://site.financialmodelingprep.com/developer/docs)
