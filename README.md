
<p align="center">
  <img src="https://github.com/user-attachments/assets/e679422b-770d-4ef9-8db3-14940681b58f" alt="Data Literacy Month AI Engineering for Grandmas" width="750">
</p>


## I ❤️ Making AI More Accessible for Beginners! 
I believe that AI should be accessible to everyone, regardless of their technical background.  The AI Engineering for Grandmas project is a step towards that vision. - Gregory Kennedy


<p align="center">
  <img src="https://github.com/user-attachments/assets/ff2f2168-e350-4ff8-9891-4994676a19a5" alt="Gregory Kennedy Data Literacy Month AI Engineering for Grandmas" width="750">
</p>



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Prompt Engineer - Quickstart Guide</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;
            line-height: 1.6;
            color: #58a6ff; /* Changed to blue */
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #0d1117;
        }
        .content {
            background-color: #161b22;
            padding: 20px;
            border-radius: 6px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .toc {
            background-color: #161b22;
            border: 1px solid #30363d;
            border-radius: 6px;
            padding: 20px;
            margin-bottom: 20px;
        }
        .toc h2 {
            margin-top: 0;
            color: #58a6ff; /* Changed to blue */
        }
        .toc ul {
            list-style-type: none;
            padding-left: 0;
        }
        .toc ul ul {
            padding-left: 20px;
        }
        .toc li {
            margin-bottom: 10px;
        }
        .toc a {
            text-decoration: none;
            color: #58a6ff;
            transition: color 0.3s ease;
        }
        .toc a:hover {
            color: #79c0ff;
        }
        h1, h2, h3, h4 {
            color: #58a6ff; /* Changed to blue */
        }
        code {
            background-color: #0d1117;
            border: 1px solid #30363d;
            border-radius: 3px;
            padding: 2px 5px;
            font-family: 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, Courier, monospace;
        }
        pre {
            background-color: #0d1117;
            border: 1px solid #30363d;
            border-radius: 6px;
            padding: 10px;
            overflow-x: auto;
        }
        @media (max-width: 600px) {
            .toc, .content {
                padding: 15px;
            }
            .toc ul ul {
                padding-left: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="content">
        <h1>AI Prompt Engineer  - Comprehensive Guide</h1>

        <div class="toc">
            <h2>Table of Contents</h2>
            <ul>
                <li><a href="#introduction">1. Introduction</a></li>
                <li><a href="#setup-and-installation">2. Setup and Installation</a></li>
                <li><a href="#user-interface-overview">3. User Interface Overview</a></li>
                <li>
                    <a href="#features">4. Features</a>
                    <ul>
                        <li><a href="#generate-prompt">4.1 Generate Prompt</a></li>
                        <li><a href="#generate-dataset">4.2 Generate Dataset</a></li>
                        <li><a href="#help-section">4.3 Help Section</a></li>
                    </ul>
                </li>
                <li><a href="#settings-and-configuration">5. Settings and Configuration</a></li>
                <li><a href="#advanced-features">6. Advanced Features</a></li>
                <li><a href="#troubleshooting">7. Troubleshooting</a></li>
                <li><a href="#best-practices">8. Best Practices</a></li>
                <li><a href="#faq">9. FAQ</a></li>
                <li><a href="#version-history">10. Version History</a></li>
                <li><a href="#possible-future-development-roadmap">11. Possible Future Development Roadmap</a></li>
                <li><a href="#community-and-support">12. Community and Support</a></li>
                <li><a href="#glossary-of-terms">13. Glossary of Terms</a></li>
                <li><a href="#conclusion">Conclusion</a></li>
            </ul>
        </div>

        <h2 id="introduction">1. Introduction</h2>
        <p>The AI Prompt Engineer  is a powerful Streamlit application designed to assist users in generating effective prompts for AI models and creating datasets for AI fine-tuning. It leverages Groq's Llama 3 AI models to provide advanced language processing capabilities.</p>
        <p>Key Features:</p>
        <ul>
            <li>Generate AI/LLM prompts using Chain of Thought (COT) methodology</li>
            <li>Generate test datasets for AI model fine-tuning</li>
            <li>Customizable settings for AI model parameters</li>
        </ul>

        <h2 id="setup-and-installation">2. Setup and Installation</h2>
        <p>To run the AI Prompt Engineer application, you'll need to set up your environment and install the necessary dependencies.</p>
        <h3>Prerequisites:</h3>
        <ul>
            <li>Python 3.11 or higher</li>
            <li>pip (Python package manager)</li>
        </ul>
        <h3>Installation Steps:</h3>
        <ol>
            <li>Clone the repository or download the source code.</li>
            <li>Install required packages:
                <pre><code>pip install streamlit groq python-dotenv langsmith pandas PyPDF2 streamlit-extras streamlit-option-menu streamlit-lottie requests</code></pre>
            </li>
            <li>Set up environment variables:
                Create a <code>.env</code> file in the project root directory and add the following:
                <pre><code>LANGCHAIN_TRACING_V2=true
LANGCHAIN_ENDPOINT=https://api.smith.langchain.com
LANGCHAIN_API_KEY=your_langchain_api_key
GROQ_API_KEY=your_groq_api_key</code></pre>
            </li>
            <li>Run the application:
                <pre><code>streamlit run v1.95-groq-prompt-engineer.py</code></pre>
            </li>
        </ol>

        <h2 id="user-interface-overview">3. User Interface Overview</h2>
        <p>The application features a clean and intuitive user interface divided into several sections:</p>
        <ul>
            <li>Header: Displays the application title and logo</li>
            <li>Navigation Menu: Horizontal menu for switching between main features</li>
            <li>Main Content Area: Changes based on the selected feature</li>
            <li>Sidebar: Contains settings and configuration options</li>
        </ul>
        <p>The navigation menu includes the following options:</p>
        <ul>
            <li>Generate Prompt</li>
            <li>Generate Dataset</li>
            <li>Help</li>
        </ul>

        <h2 id="features">4. Features</h2>

        <h3 id="generate-prompt">4.1 Generate Prompt</h3>
        <p>This feature allows users to create AI-generated prompts based on their input.</p>
        <p>How to use:</p>
        <ol>
            <li>Enter your question or task in the text area.</li>
            <li>Optionally, provide input variables (comma-separated).</li>
            <li>Click the "Generate Prompt" button.</li>
            <li>View the generated prompt and download options.</li>
        </ol>
        <p>Example input variables:</p>
        <ul>
            <li>topic, audience, tone</li>
            <li>product_name, target_market, unique_selling_point</li>
            <li>character_name, setting, genre</li>
        </ul>

        <h3 id="generate-dataset">4.2 Generate Dataset</h3>
        <p>This feature helps users create test datasets for AI model fine-tuning.</p>
        <p>How to use:</p>
        <ol>
            <li>Enter a topic or text for test data generation.</li>
            <li>Specify the number of conversation pairs to generate (1-100).</li>
            <li>Click the "Generate Test Data" button.</li>
            <li>View the generated conversation pairs.</li>
            <li>Download the data as JSON or JSONL format.</li>
        </ol>

        <h3 id="help-section">4.3 Help Section</h3>
        <p>The Help section provides detailed information on how to use the application, including:</p>
        <ul>
            <li>Step-by-step instructions for each feature</li>
            <li>Tips for achieving better results</li>
            <li>FAQ addressing common questions and concerns</li>
        </ul>

        <h2 id="settings-and-configuration">5. Settings and Configuration</h2>
        <p>The sidebar contains important settings and configuration options:</p>
        <ul>
            <li>API Key Input: Enter your Groq API key (required for functionality)</li>
            <li>Model Selection: Choose between different Groq Llama 3 model versions</li>
            <li>Temperature Slider: Adjust the creativity/randomness of the AI output (0.0 to 1.5)</li>
            <li>Max Output Tokens: Set the maximum length of the AI-generated content (1024 to 8192)</li>
        </ul>

        <h2 id="advanced-features">6. Advanced Features</h2>
        <h3>6.1 Chain of Thought (COT) Prompting</h3>
        <p>The  application utilizes Chain of Thought (COT) prompting to generate more effective and detailed AI responses. This approach breaks down complex tasks into logical steps, encouraging the AI model to show its reasoning process.</p>
        <p>Key aspects of COT prompting in :</p>
        <ul>
            <li>Task analysis and breakdown</li>
            <li>Incorporation of provided variables</li>
            <li>Adaptation to specific Groq model capabilities</li>
            <li>Optimization for clarity and specificity</li>
            <li>Inclusion of context and formatting instructions</li>
            <li>Encouragement of creativity and problem-solving</li>
            <li>Consideration of error handling and edge cases</li>
        </ul>

        <h3>6.2 Langsmith Tracing and Observability</h3>
        <p>The application integrates Langsmith for tracing and observability of AI interactions. This feature helps in monitoring and analyzing the performance of the AI prompts and responses.</p>
        <p>To enable Langsmith tracing:</p>
        <ol>
            <li>Ensure the <code>LANGCHAIN_TRACING_V2</code> environment variable is set to <code>true</code>.</li>
            <li>Provide your Langsmith API key in the <code>.env</code> file.</li>
        </ol>
        <p>Benefits of Langsmith integration:</p>
        <ul>
            <li>Track and analyze AI prompt effectiveness</li>
            <li>Identify patterns in user queries and AI responses</li>
            <li>Optimize application performance and resource usage</li>
        </ul>

        <h3>6.3 Dynamic Model Selection</h3>
        <p>Users can select different versions of the Groq Llama 3 model based on their specific needs:</p>
        <ul>
            <li>llama3-70b-8192: Large model with high performance</li>
            <li>llama3-8b-8192: Smaller model with faster inference</li>
            <li>llama3-groq-70b-8192-tool-use-preview: Specialized for tool use</li>
            <li>llama3-groq-8b-8192-tool-use-preview: Smaller tool-use model</li>
            <li>llama-3.1-8b-instant: Fast and efficient model</li>
            <li>llama-3.1-70b-versatile: Versatile model for various tasks</li>
        </ul>
        <p>The application dynamically adjusts its prompting strategy based on the selected model to leverage each version's strengths.</p>

        <h3>6.4 Adaptive Temperature and Token Management</h3>
        <p>The temperature and max output tokens settings allow for fine-tuned control over the AI's output:</p>
        <ul>
            <li>Temperature (0.0 to 1.5):
                <ul>
                    <li>Lower values: More focused and deterministic responses</li>
                    <li>Higher values: More creative and diverse outputs</li>
                </ul>
            </li>
            <li>Max Output Tokens (1024 to 8192):
                <ul>
                    <li>Adjust based on the complexity of the task and desired response length</li>
                    <li>Helps in managing API usage and response time</li>
                </ul>
            </li>
        </ul>

        <h3>6.5 Test Data Generation for AI Fine-Tuning</h3>
        <p>The test data generation feature creates structured datasets suitable for fine-tuning language models:</p>
        <ul>
            <li>Generates pairs of human messages and AI responses</li>
            <li>Outputs data in both JSON and JSONL formats</li>
            <li>Allows customization of topic and number of conversation pairs</li>
        </ul>
        <p>Use cases for generated test data:</p>
        <ul>
            <li>Fine-tuning custom AI models</li>
            <li>Evaluating AI performance on specific topics</li>
            <li>Creating benchmarks for AI system testing</li>
        </ul>

        <h2 id="troubleshooting">7. Troubleshooting</h2>
        <h3>7.1 API Key Issues</h3>
        <p>If you encounter problems related to the Groq API key:</p>
        <ol>
            <li>Ensure the API key is entered correctly in the sidebar.</li>
            <li>Check that your API key has the necessary permissions and quota.</li>
            <li>Verify your internet connection to ensure the API can be accessed.</li>
        </ol>

        <h3>7.2 Model Performance</h3>
        <p>If you're not satisfied with the model's performance:</p>
        <ol>
            <li>Try adjusting the temperature setting.</li>
            <li>Experiment with different model versions.</li>
            <li>Refine your input prompts for more specific results.</li>
        </ol>

        <h3>7.3 Application Errors</h3>
        <p>For general application errors:</p>
        <ol>
            <li>Check the console for error messages.</li>
            <li>Ensure all required packages are installed and up to date.</li>
            <li>Restart the application and try again.</li>
        </ol>

        <h2 id="best-practices">8. Best Practices</h2>
        <ul>
            <li>Start with clear, specific prompts for better results.</li>
            <li>Use the Chain of Thought methodology for complex tasks.</li>
            <li>Experiment with different model versions and settings.</li>
            <li>Regularly update the application and dependencies.</li>
            <li>Use generated datasets responsibly and ethically.</li>
        </ul>

        <h2 id="faq">9. FAQ</h2>
        <ul>
            <li>Q: How do I get a Groq API key?<br>A: Visit the Groq website and sign up for an account to obtain an API key.</li>
            <li>Q: Can I use this tool for commercial purposes?<br>A: Check the Groq API terms of service for commercial usage guidelines.</li>
            <li>Q: How often is the application updated?<br>A: Check the GitHub repository for the latest updates and release information.</li>
        </ul>

        <h2 id="version-history">10. Version History</h2>
        <ul>
            <li>v1.0: Initial release with basic prompt generation</li>
            <li>v1.5: Added dataset generation feature</li>
            <li>v1.8: Integrated Langsmith tracing</li>
            <li>v1.9: Added support for multiple Groq models</li>
        </ul>

        <h2 id="possible-future-development-roadmap">11. Possible Future Development Roadmap</h2>
        <ul>
            <li>Integration with more AI models and providers</li>
            <li>Advanced prompt templates and customization options</li>
            <li>Collaborative features for team-based prompt engineering</li>
            <li>Enhanced analytics and visualization of AI interactions</li>
        </ul>

        <h2 id="community-and-support">12. Community and Support</h2>
        <ul>
            <li>Join our community forum for discussions and support</li>
            <li>Contribute to the project on GitHub</li>
            <li>Follow us on social media for updates and tips</li>
            <li>Contact support@example.com for technical assistance</li>
        </ul>

        <h2 id="glossary-of-terms">13. Glossary of Terms</h2>
        <ul>
            <li>LLM: Large Language Model</li>
            <li>COT: Chain of Thought</li>
            <li>API: Application Programming Interface</li>
            <li>Fine-tuning: Process of adapting a pre-trained model to specific tasks</li>
            <li>Prompt: Input text that guides the AI model's response</li>
        </ul>

        <h2 id="conclusion">Conclusion</h2>
        <p>The AI Prompt Engineer  application provides a powerful toolset for creating effective AI prompts and datasets. By leveraging advanced features like Chain of Thought prompting and dynamic model selection, users can optimize their AI interactions and achieve better results in various language processing tasks.</p>
    </div>
</body>
</html>
<!---
aiengineeringforgrandmas/aiengineeringforgrandmas is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->


