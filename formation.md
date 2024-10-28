# Tutorial: Setting Up Reproducible Training Environments with the SSPCloud and notebooks

## Introduction
In the world of data science and programming, having a flexible and reproducible training environment is essential. For educators and students alike, the ability to quickly set up consistent, ready-to-use environments is a game-changer. Onyxia excels at providing such environments. With just a simple link, users can launch pre-configured training environments, making it ideal for hands-on learning. This tutorial explains why SSP Cloud and notebooks are powerful tools for training, and how to structure and deploy an effective course using these technologies.

## Why SSP Cloud for Training?
SSP Cloud allows users to deploy cloud-based workspaces easily, without the hassle of local installation or complex configuration. Here’s why it’s particularly useful for training:

1. **Instant Setup**: Instructors can share a link that configures everything—environment, software, and even datasets—so learners don’t need to install or configure anything locally.
   
2. **Consistency Across Learners**: By providing a reproducible environment, everyone works with the same configuration, minimizing setup issues that typically arise with different operating systems and dependencies.

3. **Scalability**: SSP Cloud can scale with your needs, offering powerful computing resources for large datasets or compute-intensive tasks. This allows it to support a wide range of training types, from beginner-level Python tutorials to advanced machine learning workflows.

## Which materials should be used for Trainings?

When designing a data science training program, several formats can be considered, each with distinct advantages and limitations:

- **Static PDFs and Slide Decks**: These formats are useful for delivering structured, concise theoretical content. **Advantages** include ease of distribution and low technical requirements, making them suitable for foundational material. **Inconveniences**: Lack interactivity and hands-on engagement, which are critical in data science training.

- **Video Tutorials**: Videos offer engaging, visual explanations, which are helpful for complex concepts. **Advantages**: They can simulate a classroom environment with step-by-step guidance. **Inconveniences**: Videos can become outdated quickly, and learners cannot directly interact with code or data, limiting experiential learning.

- **Interactive Websites**: Platforms like Codecademy allow learners to work with embedded code exercises and provide immediate feedback. **Advantages**: They are highly engaging and often adaptive to learners' progress. **Inconveniences**: They may require paid access and are harder to customize with specific datasets or unique content.

- **Jupyter Notebooks**: Notebooks combine explanation, code, and visualization in one interactive document, ideal for hands-on learning in data science. **Advantages**: Customizable, with interactive code cells, exercises, and immediate visualization of results, notebooks allow for experimentation directly within the learning material. **Inconveniences**: Require a setup (e.g., Jupyter or cloud platforms) and may be unfamiliar for absolute beginners.

**Conclusion**: While each format has strengths, **Jupyter Notebooks** offer a balanced, interactive approach for self-paced data science training, fostering active learning and practical experience.

| Format               | Advantages                                                                                   | Inconveniences                                                                            |
|----------------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| **Static PDFs and Slide Decks** | Easy distribution; suitable for foundational or theory-heavy content.                  | Lacks interactivity and practical application, limiting hands-on engagement.              |
| **Video Tutorials**  | Visual and engaging; provides guided, step-by-step explanations.                            | Cannot be interacted with directly; quickly outdated and often unsuitable for experimentation; hard to maintain. |
| **Interactive Websites** | Highly engaging; provides immediate feedback and adaptability based on learner progress. | Limited customization for specific content                      |
| **Jupyter Notebooks** | Interactive; combines explanation with live code, visualizations, and hands-on practice.     | Requires initial setup (cloud or local) and may be unfamiliar for beginners.              |

**Conclusion**: **Jupyter Notebooks** are often the best choice for data science training, combining interactivity and practical learning in a flexible format.


## Why use of Notebooks ? (TO DO : delete)
Notebooks have become a standard tool for education in programming and data science due to their versatility and interactive nature. Here’s why:

1. **Code and Explanation Side by Side**: Notebooks allow you to mix live code, text, images, and visualizations. Instructors can explain concepts in markdown cells while learners can run code interactively in the same document.

2. **Step-by-Step Learning**: Learners can execute code in small chunks and see the results immediately. This incremental approach is excellent for building understanding, as students can experiment and tweak code without re-running entire programs.

3. **Self-Paced and Interactive**: Notebooks encourage exploration and experimentation, allowing learners to go at their own pace. They can run the examples provided, then modify the code to see how changes affect the output, enhancing engagement.

4. **Reproducibility**: Notebooks are ideal for documenting full workflows, ensuring that learners can reproduce their results or revisit previous exercises without issues. This is crucial for both learning and research purposes.

5. **Integration with Popular Tools**: Notebooks supports multiple languages (Python, R, Julia, etc.), making it a flexible tool for teaching different programming languages and workflows. In data science, Jupyter easily integrates with libraries such as Pandas, NumPy, and Matplotlib for data manipulation and visualization.


## How to Structure an Effective Training Course with SSP Cloud notebooks

1. **Clear Objectives**: Start with clear learning objectives. For example, a Python basics course could focus on data types, control structures, and basic data manipulation using libraries like Pandas.

2. **Pre-configured Environment**: Create an SSP Cloud environment with all necessary libraries included see the [next paragraph in order to configure the environment](TO DO ADD LINK). This allows learners to focus on learning instead of dealing with setup problems.

3. **Modular Notebooks**: Break the course into several Notebooks, each covering a key concept or topic. Each notebook should have a combination of:
   - **Explanatory text**: To describe the theory and concepts behind the code.
   - **Code cells**: For learners to run, modify, and experiment with.
   - **Exercises**: Challenge students with problems to solve using the concepts they’ve learned.
   
   For example:
   - Notebook 1: Introduction to Python and data types.
   - Notebook 2: Control flow (loops, conditionals).
   - Notebook 3: Working with files and data.

4. **Step-by-Step Walkthroughs**: Each notebook should contain step-by-step instructions that learners can follow, starting with simple examples and building up to more complex exercises. Use markdown cells to explain what each piece of code does.

5. **Interactive Exercises**: Include exercises at the end of each module. Encourage learners to modify the code, test different inputs, and debug any errors they encounter.

6. **Visualizations and Data Exploration**: Make use of the visualization libraries to create engaging plots and graphs. This is especially useful when teaching data analysis, as it allows learners to immediately see the impact of their code on data.

7. **Progressive Difficulty**: Start with basic concepts and gradually introduce more advanced topics, allowing learners to build their skills step by step. This scaffolding approach ensures that students aren’t overwhelmed but are constantly challenged.






### TODO mettre le paragraphe suivant à un meilleur endroit.


Please note you can display solutions for exercises in two ways: either by creating separate files - one for exercises and another one for solutions - or by embedding the solution directly within the course using the following snippet of code:

```markdown
<details>

<summary>

Show solution

</summary>

Content of the solution

</details>
```



## Setting Up an Environment Using the SSP Cloud Platform

With SSP Cloud, you have the flexibility to create a custom, shareable link that launches a pre-configured service for learners, or, for an even smoother experience, add a link directly within a training catalog or interface. These options provide two easy paths for starting a training session:

1. **Creating a Shareable Link**: Generate a link that contains all the necessary configurations for your chosen environment, and share this link with apprentices. They can then access the environment instantly, with everything they need already set up.

2. **Embedding in a Training Catalog**: Alternatively, you can create a custom “launch” button in SSP Cloud's interface, mapped to your specific training environment. This makes it even simpler for learners to access; they just click the button to open the configured environment directly.

### How the Link Works

The setup link is a powerful feature in SSP Cloud, allowing you to define all aspects of the training environment. Here’s what it can include:

- **Service Selection**: Decide on the language and framework for the training. Options include **Python**, **PySpark**, or environments that use **GPU** resources, ideal for more computationally intensive tasks.

- **Resource Allocation**: Define the amount of computational resources required, including memory, CPU, and storage. This ensures that the environment matches the needs of the course content, even for large data sets or intensive machine learning tasks.

- **Initialization Scripts**: To ensure all learners start with the same setup, you can attach an initialization script to the link. [See here for initialization scripts examples](https://github.com/InseeFrLab/sspcloud-init-scripts). This script can:

   - Clone the training repository with all relevant notebooks and materials.

   - Install any necessary libraries, dependencies... so there’s nothing to install locally.

By clicking the link, all learners launch the exact same environment, fully configured and ready to use. This uniformity is a huge benefit in training scenarios: everyone works with the same setup, eliminating any inconsistencies that might arise from varied installations.


Here's an example link:

https://datalab.sspcloud.fr/launcher/ide/jupyter-python?autoLaunch=true&name=python-initiation&init.personalInit=%C2%ABhttps://raw.githubusercontent.com/InseeFrLab/formation-python-initiation/main/utils/init_onyxia.sh%C2%BB&init.personalInitArgs=%C2%ABen%20fundamentals%20types-variables%C2%BB&security.allowlist.enabled=false


This link automatically launches a **Jupyter Notebook** environment on the sspcloud and configures it with pre-installed libraries and scripts, thanks to the `init.personalInit` argument. Note : you can change it to Vscode if you prefer.

- **Predefined Content**: The link includes initialization scripts that set up a predefined training module, in this case, "Python Fundamentals: Types and Variables". All learners will start with this exact configuration.
- **No Setup Required**: This eliminates the common issues of dependency mismatches and local installation errors, so learners can jump directly into the material.

## Add your Training course on the SSP Cloud platform 

In order to add a tutorial on the [SSP Cloud dedicated place] (https://www.sspcloud.fr/formation) you can [submit a PR on github](https://github.dev/InseeFrLab/www.sspcloud.fr/blob/main/src/lib/getHelmDatasciencePackageCount.ts).

There, you'll have the possibility to define the name of your course, fill an abstract to inform the users of its content, specify the authors, the date of creation of the course, to add tags and keywords... To set an image to represent the course, the number of expected hours to follow the course and an article URL if you want to direct the users to an external resource to explain the content of the course. (TO DO ADD A PICTURE - READ + LAUNCH BUTTON) And finally give the URL to launch the preconfigured service.  🚀️


To organize the course effectively, you can divide it into different **parts**. Use this feature to group related tutorials within a course folder, allowing learners to follow a structured, progressive format.

For example, you can follow this pattern 

``` yaml

 {
        "name": {
            "fr": "Nom d'un dossier contenant des cours",
            "en": "Name of a folder traing",
        },
        "abstract": {
            "fr": "Description de ce que contient le dossier.",
            "en": "Description of the content of the folder.",
        },
        "imageUrl": anImgUrl,
        "tags": ["learn", "discover"],
        "parts": [
            {
                "name": {
                    "fr": "1. Un titre descriptif pour la première partie de la formation",
                    "en": "1. A descriptive title for the first part of the course",
                },
                "abstract": {
                    "fr": "Ici se trouve une description de la première partie de la formation",
                    "en": "Here lies a description of the first part of the course",
                },
                "authors": ["Inseefrlab"],
                "types": ["Notebook Python"],
                "tags": ["discover", "learn"],
                "category": "Discover the platform",
                "imageUrl": anImgUrl,
                "timeRequired": 1,
                "deploymentUrl": {
                    "fr": "https://datalab.sspcloud.fr/launcher/ide/jupyter-python?autoLaunch=true&init.personalInit=«https://raw.githubusercontent.com/InseeFrLab/myinitscript",
                    "en": "https://datalab.sspcloud.fr/launcher/ide/jupyter-pyspark?autoLaunch=true&init.personalInit=«https://raw.githubusercontent.com/InseeFrLab/InseeFrLab/myinitscript",
                },
            },
            {
                "name": {
                    "fr": "2. Un titre descriptif pour la seconde partie de la formation",
                    "en": "2. A descriptive title for the second part of the course",
                },
                "abstract": {
                    "fr": "Ici se trouve une description de la deuxième partie de la formation",
                    "en": "Here lies a description of the second part of the course",
                },
                "authors": ["Inseefrlab"],
                "types": ["Notebook Python"],
                "tags": ["discover", "learn"],
                "category": "Discover the platform",
                "imageUrl": anImgUrl,
                "timeRequired": 1,
                "deploymentUrl": {
                    "fr": "https://datalab.sspcloud.fr/launcher/ide/jupyter-python?autoLaunch=true&init.personalInit=«https://raw.githubusercontent.com/InseeFrLab/myinitscript",
                    "en": "https://datalab.sspcloud.fr/launcher/ide/jupyter-pyspark?autoLaunch=true&init.personalInit=«https://raw.githubusercontent.com/InseeFrLab/InseeFrLab/myinitscript",
                },
            },
...
]

```

## To add somewhere - The data 📁️

If your course requires data, you can make it accessible either by sharing a public link (allowing open access) or by placing the data in a "diffusion" folder within your bucket repository on the platform. This second option automatically makes the data available to all SSP Cloud users, providing seamless integration within the platform environment and consequently reduce the network traffic.

## Conclusion
The SSP Cloud combined with Notebooks creates an ideal environment for teaching and learning programming or data science. The combination of instant, cloud-based environments with the interactive nature of notebooks allows for engaging, reproducible, and scalable training sessions. By leveraging these tools, educators can focus on what matters most, eg teaching and learning, without worrying about setup issues or inconsistent environments. 

For your next training session, try setting up your environment using the SSP Cloud, and see how they can transform the learning experience! 👩‍🎓️

