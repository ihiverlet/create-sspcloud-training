# Tutorial: Setting Up Reproducible Training Environments with the SSPCloud and notebooks

## Introduction
In the world of data science and programming, having a flexible and reproducible training environment is essential. For educators and students alike, the ability to quickly set up consistent, ready-to-use environments is a game-changer. Onyxia excels at providing such environments. With just a simple link, users can launch pre-configured training environments, making it ideal for hands-on learning. This tutorial explains why SSP Cloud and notebooks are powerful tools for training, and how to structure and deploy an effective course using these technologies.

## Why SSP Cloud for Training?
SSP Cloud allows users to deploy cloud-based workspaces easily, without the hassle of local installation or complex configuration. Here’s why it’s particularly useful for training:

1. **Instant Setup**: Instructors can share a link that configures everything—environment, software, and even datasets—so learners don’t need to install or configure anything locally.
   
2. **Consistency Across Learners**: By providing a reproducible environment, everyone works with the same configuration, minimizing setup issues that typically arise with different operating systems and dependencies.

3. **Scalability**: SSP Cloud can scale with your needs, offering powerful computing resources for large datasets or compute-intensive tasks. This allows it to support a wide range of training types, from beginner-level Python tutorials to advanced machine learning workflows.

## Which materials should be used for Trainings?

When designing effective training materials, it’s crucial to select formats that engage learners and enhance comprehension. Even though PDFs, slide decks, and videos all offer valuable ways to present information, we will focus on interactive environments as they are ideal for practical training. Interactive environments allow learners to apply concepts immediately, test code in real time, and actively participate in their learning journey which promotes deeper understanding and skill retention. 

In the following, we'll compare different interactive environments according to the language used. Will also be shown a way to deploy a static site on the platform using quarto. 

### 🚧 WIP - Deploy a static site using quarto - WIP 
Here will lie some explanation on how to deploy a static site using quarto and CI to automate its deployment.
### End of WIP 🚧

### Using Python 

🐍 In python, Jupyter Notebooks, also available in Vscode, stand out as the go-to choice. With support for rich media, widgets, and numerous extensions, it allows the integration of interactive graphs, data tables, and even forms for exercises.


### Using R 

®️ In R, we can either use Rmarkdown Notebooks or LearnR which offers interactive tutorials embedded within R Markdown documents. Both of them combine explanation, code and visualization in an interactive document. However, even if learnR allows to generate interactive and more complexe elements such as quizzes making it ideal for beginner tutorials, it requires the deployment of a Shiny server which can be costly. Moreover, in learnR cells do not communicate across the entire environment hence defining global variables or managing state becomes challenging. This restriction limits the effectiveness of learnr for complex tutorials where a connected, evolving state is necessary to build on previous steps.

Overall, while learnR provides an interactive environment for R that’s suitable for simple exercises, Rmarkdown Notebooks offer a more robust, flexible, and widely-used solution. For R, traditional R Markdown or local interactive sessions are often more practical for comprehensive training sessions. 
This is why, for sophisticated training materials that require smooth progression and state management, notebooks remains the preferred choice for Python or R tutorials.

## How to Structure an Effective Training Course with SSP Cloud notebooks

1. **Clear Objectives**: 👨‍🎓 Start with clear learning objectives. For example, a Python basics course could focus on data types, control structures, and basic data manipulation using libraries like Pandas.

2. **Pre-configured Environment**: Create an SSP Cloud environment with all necessary libraries included see the [next paragraph in order to configure the environment](TO DO ADD LINK). This allows learners to focus on learning instead of dealing with setup problems.

3. **Modular Notebooks**: 📚 Break the course into several Notebooks, each covering a key concept or topic. Each notebook should have a combination of:
   - **Explanatory text**: To describe the theory and concepts behind the code.
   - **Code cells**: For learners to run, modify, and experiment with.
   - **Exercises**: Challenge students with problems to solve using the concepts they’ve learned.
   
   For example:
   - Notebook 1: Introduction to Python and data types.
   - Notebook 2: Control flow (loops, conditionals).
   - Notebook 3: Working with files and data.

4. **Step-by-Step Walkthroughs**: 👣 Each notebook should contain step-by-step instructions that learners can follow, starting with simple examples and building up to more complex exercises. Use markdown cells to explain what each piece of code does.

5. **Interactive Exercises**: Include exercises at the end of each module. Encourage learners to modify the code, test different inputs, and debug any errors they encounter.

You can display solutions for exercises in two ways: either by creating separate files - one for exercises and another one for solutions - or by embedding the solution directly within the course using the following snippet of code:

```markdown
<details>

<summary>

Show solution

</summary>

Content of the solution

</details>
```

6. **Visualizations and Data Exploration**: 🔎 Make use of the visualization libraries to create engaging plots and graphs. This is especially useful when teaching data analysis, as it allows learners to immediately see the impact of their code on data.

7. **Progressive Difficulty**: 📈 Start with basic concepts and gradually introduce more advanced topics, allowing learners to build their skills step by step. This scaffolding approach ensures that students aren’t overwhelmed but are constantly challenged.


## Setting Up an Environment Using the SSP Cloud Platform

With SSP Cloud, you have the flexibility to create a custom, shareable link that launches a pre-configured service for learners, or, for an even smoother experience, add a link directly within tutorials referential. These options provide an easy path for starting a training session.

1. **Generate a link** that contains all the necessary configurations for your chosen environment, and share this link with apprentices. They can then access the environment instantly, with everything they need already set up.

2. **Share this link** with the learners. You can create your own tutorial referential by publishing them through a GitHub repository, using a static website, or [adding them to the Tutorials Section on the SSP Cloud Platform](TO DO: ADD LINK to "Add your Training Course on the SSP Cloud Platform"). By choosing the latter, you can create a custom “launch” button within SSP Cloud's interface, mapped to your specific training environment. This makes it even easier for learners to access—just one click opens the configured environment directly.

The possibilities for sharing your links are endless. Choose the one that best fits your needs! ✨

### How the Link Works

The setup link is a powerful feature in SSP Cloud, allowing you to define all aspects of the training environment. In order to get your link, feel free to use the SSP Cloud platform and configure a service. Then click on the `Copy auto launch URL` button. 
By clicking the link, all learners launch the exact same environment, fully configured with the specified configuration and ready to use. This uniformity is a huge benefit in training scenarios: everyone works with the same setup, eliminating any inconsistencies that might arise from varied installations.


The link can include :
- service selected to decide on the language and framework for the training
- the resources to define the amount of computational resources required, including memory, CPU, and storage. This ensures that the environment matches the needs of the course content, even for intensive machine learning tasks
- an initialization script to ensure all learners start with the same setup. [See here for initialization scripts examples](https://github.com/InseeFrLab/sspcloud-init-scripts). This script can:
    - Clone the training repository with all relevant notebooks and materials.
    - Install any necessary libraries, dependencies... so there’s nothing to install locally.
- and many more ...


Here's an example link: ## TODO METTRE UN LIEN AVEC UN VSCODE

https://datalab.sspcloud.fr/launcher/ide/jupyter-python?autoLaunch=true&name=python-initiation&init.personalInit=%C2%ABhttps://raw.githubusercontent.com/InseeFrLab/formation-python-initiation/main/utils/init_onyxia.sh%C2%BB&init.personalInitArgs=%C2%ABen%20fundamentals%20types-variables%C2%BB&security.allowlist.enabled=false

This link automatically launches a **Jupyter Notebook** environment on the sspcloud and configures it with pre-installed libraries and scripts, thanks to the `init.personalInit` argument. Note : you can change it to Vscode if you prefer.

- **Predefined Content**: The link includes initialization scripts that set up a predefined training module, in this case, "Python Fundamentals: Types and Variables". All learners will start with this exact configuration.
- **No Setup Required**: This eliminates the common issues of dependency mismatches and local installation errors, so learners can jump directly into the material.

## Publish Your Training Course in the Tutorials Section on the SSP Cloud Platform 

In order to add a tutorial on the [SSP Cloud dedicated place] (https://www.sspcloud.fr/formation) you can [submit a PR on github](https://github.dev/InseeFrLab/www.sspcloud.fr/blob/main/src/lib/getHelmDatasciencePackageCount.ts).

There, you'll have the possibility to define the name of your course, fill an abstract to inform the users of its content, specify the authors, the date of creation of the course, to add tags and keywords... To set an image to represent the course, the number of expected hours to follow the course and an article URL if you want to direct the users to an external resource to explain the content of the course. (TO DO ADD A PICTURE - READ + LAUNCH BUTTON) And finally give the URL to launch the preconfigured service.  🚀️


To organize the course effectively, you can divide it into different parts. Use this feature to group related tutorials within a course folder, allowing learners to follow a structured, progressive format.

For example, you can follow this pattern 

``` yaml

 {
        "name": {
            "fr": "Nom d'un dossier contenant des cours",
            "en": "Name of a folder training",
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

### Make your data available to everyone 📁️

If your course requires data, you can make it accessible either by sharing a public link (allowing open access) or by placing the data in a "diffusion" folder within your bucket on the platform. This second option automatically makes the data available to all SSP Cloud users, providing seamless integration within the platform environment and consequently reduce the network traffic.

[Click here for more information](https://docs.sspcloud.fr/en/content/storage.html#sharing-data)

## Conclusion
The SSP Cloud combined with Notebooks creates an ideal environment for teaching and learning programming or data science. The combination of instant, cloud-based environments with the interactive nature of notebooks allows for engaging, reproducible, and scalable training sessions. By leveraging these tools, educators can focus on what matters most, eg teaching and learning, without worrying about setup issues or inconsistent environments. 

For your next training session, try setting up your environment using the SSP Cloud, and see how they can transform the learning experience! 👩‍🎓️

