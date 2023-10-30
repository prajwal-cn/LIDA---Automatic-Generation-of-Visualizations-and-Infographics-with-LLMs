# LIDA: Generate Visualizations from Data Using LLMs - Streamlit App

<img width="886" alt="image" src="https://github.com/prajwal-cn/LIDA---Automatic-Generation-of-Visualizations-and-Infographics-with-LLMs/assets/127007794/c8a50ff0-c5c7-4fe2-ab0b-383b1ce6c50a">

LIDA is a library for generating data visualizations and data-faithful infographics using Large Language Models (LLMs). It is grammar agnostic and works with multiple LLM providers and visualization libraries.

## Why use LIDA?
LIDA offers a number of advantages over traditional methods of generating data visualizations:

It is easy to use: LIDA provides a simple API that makes it easy to generate visualizations even for users with no programming experience.
It is flexible: LIDA can generate a wide variety of visualizations, including charts, graphs, infographics, and data stories.
It is scalable: LIDA can generate visualizations from datasets of any size.
It is accurate: LIDA uses LLMs to generate visualizations that are accurate and data-faithful.
How to use LIDA
To use LIDA, simply follow these steps:

## Install LIDA:

`pip install lida`

## Choose an LLM provider:

LIDA supports multiple LLM providers, including OpenAI, Azure OpenAI, PaLM, Cohere, and Huggingface. To choose an LLM provider, set the text_gen parameter to the name of the provider when initializing the LIDA manager. For example, to use OpenAI, you would do the following:

Python
`from lida import Manager`

`lida = Manager(text_gen="openai")`
Use code with caution. Learn more
Load your data:
LIDA can work with any type of data, including CSV files, Pandas DataFrames, and SQL databases. To load your data, simply pass it to the summarize() method.

Python
`summary = lida.summarize("data/cars.csv")`

Generate visualization goals:
LIDA can automatically enumerate visualization goals given the data. To do this, simply call the goals() method.

Python
`goals = lida.goals(summary)`

Generate visualization code:
LIDA can generate visualization code in a variety of visualization libraries, including matplotlib, seaborn, altair, and d3. To generate visualization code, simply call the visualize() method.

Python
`charts = lida.visualize(summary, goals=goals)`

Execute and refine the visualization:
LIDA can execute the generated visualization code and refine it as needed. To do this, simply call the render() method.

Python
`lida.render(charts)`

This will save the visualizations to the current directory. You can then open the visualizations in a web browser or image viewer.

Example
Python
`import lida`

# Load the data
`summary = lida.summarize("data/cars.csv")`

# Generate visualization goals
`goals = lida.goals(summary)`

# Generate visualization code
`charts = lida.visualize(summary, goals=goals)`

# Execute and refine the visualization
`lida.render(charts)`

Best practices
Here are some best practices for using LIDA:

- Choose the right LLM provider: LIDA supports multiple LLM providers, each with its own strengths and weaknesses. Choose an LLM provider that is appropriate for your data and goals.

- Load clean and well-formatted data: LIDA will produce better results if you load clean and well-formatted data.
Be specific about your visualization goals: The more specific you are about your visualization goals, the better LIDA will be able to generate a visualization that meets your needs.

- Review and refine the generated visualization code: LIDA will generate visualization code that is accurate and data-faithful, but it is a good idea to review and refine the code before executing it.

- Use LIDA's advanced features: LIDA provides a number of advanced features, such as visualization editing, explanation, evaluation, and recommendation. Take advantage of these features to create the best possible visualizations.
  
## Conclusion

LIDA is a powerful tool for generating data visualizations and infographics using LLMs. It is easy to use and provides a variety of features that make it a valuable tool for data scientists, analysts, and journalists.
