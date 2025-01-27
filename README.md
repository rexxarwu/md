# Global Stock Market Agent

## Project Introduction
This project aims to automate the analysis of global stock market. It applies the multi-agent technique with pre-defined functions as tools to finish the tasks of data retrieval, analysis, visualization and generation of report.

---

## Project Goals
1. Extract the financial data and company details with given pre-defined funtions.
2. Streamline the analysis process using two agents specializing in executing and analyzing seperately, to enhance the proficiency and optimize the resource usage.
3. Generate structured and comprehensive report regarding global stock market and predict the trends.

---

## Project Steps

### Environment Setup
- **Setup Instructions**: Install the library: pyautogen, finrobot, finnhub-python, sec-api and all the dependencies.
- **Commands or Tools to Install and Activate**:
  - pip in Python environment.
  - "!pip install {lib}" in colab for cloud-based execution.

### Framework Configuration
- **Agent Registration**:
  - **Agent 1**: user proxy to execute python functions and control the conversations.
  - **Agent 2**: market analyst who possesses strong analytical and problem-solving abilities
- **API Key Configuration**:
  - OpenAI API keys for analysis (limited and paid). Here we create an environment file and set the OpenAI API key in it.
  - finnhub_api which is free. (https://finnhub.io/docs/api)

### Data Retrieval
- Connect to finnhub-api that provides tools grabbing real company news, financials and profiles.
- Use the yahoo finance tool under the data-source section of finrobot to get stock data.
- Use manually-defined functions as tools to restrict the agent's behaviors to obtain desired data format for further analysis.

### Data Analysis
- Using prompts to let the market analyst agent analyze the obtained data and generates a report.
- Perform calculations and predict the trends using statistical methods. (Done by the expert agent)

### Report Generation
- Format the analyzed data into different sections for more specific analysis.
- Give clear instructions on the sections that the report should include to let the agent generate corresponding report.
- Include companies all over the world taht ensures adequate data for the analyst agent to do a prediction of the global stock market.

### Testing and Validation
- Validate data retrieval outputs against source records.
- Test the pre-defined tools applied to ensure the coherence of data transfer. Note: the register_toolkit function returns str type, which might not meet the requirment of return type.
- Use the data in the past to see how accurate the prediction is.

---

## Notes
1. Ensure API keys are securely stored and rotated periodically to maintain security.
2. The functions used are still in active updates, so that modifications would be necessary to keep up with the new function definitions.
3. Include detailed documentation to facilitate maintenance and scalability.
4. Add manually defined functions to restrict the agent's behaviors.

---

## References
1. *Gen101*, (https://citrine-music-bce.notion.site/GenAI-101-129ebcc111348119b72cf397bd7a83a3)
2. *Finnhub API*, (https://finnhub.io/docs/api)
