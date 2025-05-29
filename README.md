# LUCY Devtools

Docker image and utils for ROS development

---

## 📌 Overview

LUCY Devtools is a set of tools and scripts designed to facilitate the development of ROS-based applications.

It provides a Docker environment tailored for ROS development, along with a collection of scripts to manage the development environment efficiently.

---

## 🚀 Features

### Docker

Two dockerfile used for ROS development environment

Dockerfile are made for both Humble and Jazzy ROS distributions.

### Scripts

- ChangeEnv: Use to switch easily between ROS distributions
- Env: Use to manage environment (docker)
- InitEnv: Use to initialize the environment (must be curled from the repository)
- Make: Use to build (with colcon)
- ResetPerm: Use to setup permissions for the repository

---

## 📥 Setup

### Full setup (recommended)

```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/Sentience-Robotics/lucy_devtools/refs/heads/master/lucy_utils/InitEnv)"
```

### Basic setup

> [!WARNING]
> This setup is for advanced users who are familiar with the LUCY tools and ROS environment.

Clone the repository

```bash
git clone https://github.com/Sentience-Robotics/lucy_micro_ros_pico.git lucy_devtools
```

---

## 📖 Documentation

For more details on creation processes, troubleshooting, and other guidance, visit the [Sentience Robotics documentation](https://docs.sentience-robotics.fr).

---

## 📜 Code of Conduct

We value the participation of each member of our community and are committed to ensuring that every interaction is respectful and productive. To foster a positive environment, we ask you to read and adhere to our [Code of Conduct](CODE_OF_CONDUCT.md).

By participating in this project, you agree to uphold this code in all your interactions, both online and offline. Let's work together to maintain a welcoming and inclusive community for everyone.

If you encounter any issues or have questions regarding the Code of Conduct, please contact us at [contact@sentience-robotics.fr](mailto:contact@sentience-robotics.fr).

Thank you for being a part of our community!

---

## 🤝 Contributing

To find out more on how you can contribute to the project, please check our [CONTRIBUTING.md](CONTRIBUTING.md)

---

## 📜 License

This project is licensed under the **GNU GPL V3 License**. See the [LICENSE](LICENSE) file for details.

---

## 🙌 Acknowledgments
<!-- Add, as needed, the peoples, organisation or projects that helped this project -->

- 🎉 [InMoov Project](https://inmoov.fr/) – Original design by Gael Langevin<br>
- 🎉 **All contributors** to the InMoov community<br>

---

## 📬 Contact

- 📧 Email: [contact@sentience-robotics.fr](mailto:contact@sentience-robotics.fr)<br>
- 🌍 GitHub Organization: [Sentience Robotics](https://github.com/sentience-robotics)<br>


---

[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.0-4baaaa.svg)](code_of_conduct.md)
