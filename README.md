# 🌳 **Tree of Thoughts for Quadratic Equation Solver**

This repository demonstrates how to use **Tree of Thoughts (ToT)** combined with **LangChain** to solve quadratic equations in a more structured and reflective way.

## 📖 **Overview**

The **Tree of Thoughts (ToT)** is an advanced prompt engineering technique that guides a model through a series of thoughts or steps before reaching a conclusion. This technique decomposes complex problems into smaller sub-questions, explores each branch, and then converges on the best solution.

In this project, we use ToT to solve a quadratic equation step by step, first by reflecting on the different methods available (discriminant, factorization, completing the square), and then selecting the most appropriate one.

## ⚙️ **Techniques Used**

1. **🌳 Tree of Thoughts (ToT)**: To structure the reasoning process, breaking down the problem into multiple possible solutions and selecting the most appropriate one.
2. **🔗 LangChain**: A powerful framework used to orchestrate language models and chain them together to perform more complex tasks like reasoning and decision-making.
3. **🔢 Quadratic Equation Solving**: The problem solved involves finding the solutions to a quadratic equation of the form \( ax^2 + bx + c = 0 \).

## 🧠 **How It Works**

### 🔍 **Problem Breakdown with ToT**

The first step in solving the quadratic equation is to reflect on the different methods available. The methods are:

1. **📐 Discriminant Method**: Using the discriminant formula to find the roots of the equation.
2. **🧮 Factorization Method**: Factoring the quadratic expression if possible to find the roots.
3. **🔲 Completing the Square Method**: Converting the quadratic equation into a perfect square to find the roots.

### 🔗 **LangChain Implementation**

We use LangChain to create a chain of thought for each of these methods, guiding the model to explore and reflect on each one. The flow is as follows:

1. **💭 Reflection**: The model reflects on which methods can be applied to solve the equation.
2. **🏃 Execution**: The model runs each method step by step, explaining the process and finding the roots.
3. **📊 Evaluation**: After the methods are executed, the results are compared to select the best solution.

### 📝 **Example**


# Example quadratic equation
probleme = "2x^2 + 4x - 6 = 0"

# Reflection on methods
reflection_response = reflection_chain.run(probleme)

# Execution of each method
discriminant_response = discriminant_chain.run(probleme)
factorisation_response = factorisation_chain.run(probleme)
completer_carre_response = completer_carre_chain.run(probleme)

# Output results for each method
print("Reflection on methods:", reflection_response)
print("Discriminant method result:", discriminant_response)
print("Factorization method result:", factorisation_response)
print("Completing the square method result:", completer_carre_response)


## 🚀 **Running the Code**
 1.Clone this repository to your local machine.
 2.Install the dependencies : pip install langchain openai langchain_openai
 3.Start your LLM model server locally using LM Studio or your chosen environment.
  * For LM Studio:
    Open LM Studio and load your model configuration.
    Start the server and ensure it’s accessible, for example at http://localhost:1234/v1/ (or any other port you’ve configured).
    In your Python script, the model is loaded as follows: llm = ChatOpenAI(temperature=0.001, base_url="http://localhost:1234/v1/", api_key="not-needed")
    Ensure your LLM server is running on the correct port (1234 in this example).
 4.Run the code.ipynb script to see the reflection, execution, and evaluation of methods for solving a quadratic equation.

## 📊 **Results**
The code will output the results for each method used to solve the quadratic equation, including the reflections on the methods, the step-by-step execution of each, and the final evaluation of the solutions.

## 👨‍💻 **Authors**  
Syphax - Création initiale - [syphaxlch](https://github.com/syphaxlch)
