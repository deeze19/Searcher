#Searcher

Welcome to Searcher, your privacy-focused metasearch engine designed to deliver a secure and customizable search experience. Developed as an evolution of the SearXNG project, Searcher empowers users with the ability to take control of their online searches while prioritizing privacy and flexibility.

Contributors:
- Deborah Ezekiel - [deeze2@morgan.edu]
- Kenneth Burwell - [kebur17@morgan.edu]
- Oluwadara Dina - [oldin1@morgan.edu]

## Original Project - Searxng

The foundation of Searcher is built upon the open-source project Searxng, which is a privacy-respecting, hackable metasearch engine. We express our gratitude to the contributors of Searxng for providing the groundwork for our project.
## Features
We have made several modifications and enhancements to adapt the original Searxng to our specific project requirements. These changes include:
Project Renaming:
The original project, SearXNG, has been renamed to "Searcher" for the purpose of this assignment. This includes changes to website index names, user names, and references within the codebase.
Project Theme:
The theme of the project has been altered to align with the specific requirements of our school assignment. This may involve adjustments to the user interface, color schemes, or other design elements to suit the desired theme.
Secret Key Modification:
To enhance security, the original secret keys within the project have been changed. This includes the server's secret key, which is a crucial element for ensuring secure communication and data integrity.
Installation of Missing Dependencies:
During the setup process, it was identified that certain dependencies were missing. These dependencies have been installed to ensure the proper functioning of the Searcher instance.
These requirements included:
	certifi==2023.7.22
	babel==2.13.1
	flask-babel==4.0.0
	flask==3.0.0
	jinja2==3.1.2
	lxml==4.9.3
	pygments==2.16.1
	python-dateutil==2.8.2
	pyyaml==6.0.1
	httpx[http2]==0.24.1
	Brotli==1.1.0
	uvloop==0.19.0
	httpx-socks[asyncio]==0.7.7
	setproctitle==1.3.3
	redis==4.6.0
	markdown-it-py==3.0.0
	typing_extensions==4.8.0
	fasttext-predict==0.9.2.1
	pytomlpp==1.0.13

Logo Design and Favicon Changes:
The project's logo design has been modified to better reflect the intended theme or branding for the assignment. Additionally, the favicon, the small icon displayed in a browser tab, has been updated to align with the new logo design.
Server Port Modification:
The default server port, where the Searcher instance is hosted, has been changed. This adjustment may be made for various reasons, such as avoiding conflicts with other services or adhering to specific project requirements.
Search method:
The search method has been changed to "GET" for improved functionality.
Autocomplete:
Autocomplete has been set to use DuckDuckGo for a more enhanced search experience.
Footer Editing:
The footer of the Searcher instance has been edited to include relevant information or branding specific to the school assignment. This includes names of authors and any other information deemed important.
Addition of Cursor CSS:
A custom cursor style, defined by CSS (Cascading Style Sheets), has been added to enhance the visual experience of the Searcher instance. This could be a unique cursor design that aligns with the project theme.













## Features of Searcher
Using Searcher offers several security benefits, making it an attractive choice, especially when prioritizing privacy and control over your search queries. Here are key points highlighting the importance of using Searcher from a security perspective:
  Decentralized Control:
●	Hosting Searcher locally or on a private server gives users decentralized control. This means that individuals or organizations have the power to manage and secure their search infrastructure without relying on external entities.
  Enhanced Privacy Measures:
●	Searcher is designed with a focus on privacy. It minimizes the collection of user data, reducing the risk of exposure to third-party entities. This commitment to privacy is crucial in an era where online activities are increasingly scrutinized.
  Open-Source Transparency:
●	Searcher being open-source allows users to inspect the source code, ensuring transparency in its operations. Security-conscious users can audit the code, identify vulnerabilities, and contribute to the improvement of the project's security.
  Reduced Tracking and Profiling:
●	By avoiding the use of external trackers and analytics, Searcher helps reduce the risk of user tracking and profiling. Users can conduct searches without being subject to the extensive tracking mechanisms employed by some commercial search engines.
  User-Defined Filters:
●	Searcher's customizable nature extends to user-defined filters, enabling users to implement additional security measures. This could include content filtering, blacklisting specific domains, or incorporating custom security modules as needed.
  No Third-Party Dependencies:
●	Searcher minimizes reliance on external services or APIs for search functionality. This reduces the attack surface and potential vulnerabilities associated with third-party integrations, contributing to a more secure overall environment.
  Community-Driven Security Updates:
●	The open-source nature of Searcher encourages a community of contributors who can actively address security concerns. This collaborative approach to development ensures that security updates and patches are promptly implemented.
  Encrypted Search Connections:
●	Searcher supports encrypted search connections (HTTPS), providing a secure communication channel between the user and the search engine. This prevents potential eavesdropping and man-in-the-middle attacks during the search process.
  No Profiling for Targeted Ads:
●	Unlike some commercial search engines that use search data for targeted advertising, Searcher does not engage in such practices. This protects users from personalized advertising based on their search history.
  User Education and Empowerment:
●	Searcher places emphasis on user education, empowering individuals to make informed decisions about their online security and privacy. The platform encourages users to take an active role in understanding and managing their digital footprint.
In summary, Searcher empowers users with a secure and customizable search experience, offering the ability to host locally, customize features, obfuscate IP addresses, search images without external redirects, and maintain control over search queries. These security features collectively contribute to a more private and secure online search experience, aligning with the growing emphasis on user privacy in the digital age.



















## Installation
How to Install Searcher:
Clone the Repository:
●	Start by cloning the Searcher repository to your local machine. 
●	Use the following command in your terminal or command prompt:
Install Packages:
  $ sudo apt-get update 

  $ sudo -H apt-get install -y \
      python3-dev python3-babel python3-venv \
      uwsgi uwsgi-plugin-python3 \
      git build-essential libxslt-dev zlib1g-dev libffi-dev libssl-dev

Create User:
  $ sudo -H useradd --shell /bin/bash --system \
      --home-dir "/usr/local/searcher" \
      --comment 'Privacy-respecting metasearch engine' \
      searcher
  $sudo git clone [repository_url] "/usr/local/searcher/searxng-src"
  $ sudo -H chown -R "searcher:searcher" "/usr/local/searcher"

Install Dependencies:
  $ sudo -H -u searcher –i
  (searcher)$ python3 -m venv "/usr/local/searcher/searx-pyenv"
  (searcher)$ echo ". /usr/local/searcher/searx-pyenv/bin/activate" \
                     >>  "/usr/local/searcher/.profile"

  Exit bash and open a new one.
  $ sudo -H -u searcher -i

  (searcher)$ command -v python && python –version
  OUTPUT: “/usr/local/searcher/searx-pyenv/bin/python”
  Python 3.8.1







  # update pip's boilerplate ..
  pip install -U pip
  pip install -U setuptools
  pip install -U wheel
  pip install -U pyyaml

  # jump to Searcher’s working tree and install Searcher into virtualenv
  (searcher)$ cd "/usr/local/searcher/searxng-src"
  (searcher)$ pip install -e .

  Exit bash and open a new one.
Set secret key:
  $ sudo -H mkdir -p "/etc/searcher"
  $ sudo -H cp "/usr/local/searcher/searxng-src/utils/templates/etc/searxng/settings.yml"  "/etc/searcher/settings.yml"

      Edit config: sudo nano "/etc/searcher/settings.yml" 
      Edit config: sudo nano "/usr/local/searcher/searxng-src/utils/templates/etc/searxng/settings.yml" 

       NB: you can use the command “openssl rand -base64 21” to create your secret key


Test run:
  # enable debug ..
  $ sudo -H sed -i -e "s/debug : False/debug : True/g" "/etc/searcher/settings.yml"

  # start webapp
  $ sudo -H -u searcher -i
  (searcher)$ cd /usr/local/searcher/searxng-src
  (searcher)$ export SEARXNG_SETTINGS_PATH="/etc/searcher/settings.yml"

              Edit secret key again under: "/etc/searcher/settings.yml"

  (searcher)$ python searx/webapp.py

  # disable debug
  $ sudo -H sed -i -e "s/debug : True/debug : False/g" "/etc/searcher/settings.yml"








Navigate to Project Directory:
●	Change your current working directory to the Searcher project directory:
cd searcher


Activate Virtual Environment:
●	If you haven't activated the virtual environment, do so using the following command:
source /path/to/your/searcher-pyenv/bin/activate

●	Replace "/path/to/your/searcher-pyenv/" with the actual path to your virtual environment.



Start the Searcher Webapp:
●	Once the virtual environment is activated, start the Searcher web application. Use the following commands:
cd /path/to/your/searcher-src
python searcher/webapp.py

●	Access the web app by navigating to http://127.0.0.1:8989 in your web browser.

Explore Searcher:
●	The Searcher web interface should now be accessible. You can enter search queries in the search bar and hit enter to get results.
Customize Settings (Optional):
●	If you want to customize Searcher further, explore the configuration files in "/etc/searcher/" and modify the settings.yml file.

Shutdown the Webapp:
●	When you're done using Searcher, you can shut down the webapp. Return to the terminal where it's running and press Ctrl + C to stop the process.
Deactivate Virtual Environment (Optional):
●	If you activated a virtual environment, you can deactivate it using the following command:
deactivate

To run your application without opening the terminal manually after a system restart, you can set up your application as a system service. This way, the service manager (like systemd) will take care of starting and managing your application.

Create a systemd Service File: Create a file with a .service extension, for example, searcher.service, in the /etc/systemd/system/ directory:

sudo nano /etc/systemd/system/searxng.service 

Add the following content to the searcher.service file:

[Unit]
Description=Searcher Metasearch Engine
After=network.target

[Service]
User=searcher
Group=searcher
Environment="SEARXNG_SETTINGS_PATH=/etc/searcher/settings.yml"
WorkingDirectory=/usr/local/searcher/searxng-src
ExecStart=/usr/local/searcher/searx-pyenv/bin/python /usr/local/searcher/searxng-src/searx/webapp.py
Restart=always

[Install]
WantedBy=multi-user.target

Adjust the paths and settings according to your setup.
Reload systemd:

sudo systemctl daemon-reload 

Enable and Start the Service:
sudo systemctl enable searcher 
sudo systemctl start searcher

This will enable the service to start on boot and start it immediately.
Now, your searcher application should run as a background service, and you don't need to open the terminal after a system restart. You can manage the service using commands like sudo systemctl start searcher, sudo systemctl stop searcher, sudo systemctl restart searcher, etc.
Make sure to monitor the logs using journalctl -u searcher.service in case you need to troubleshoot any issues. Adjust the service file and settings as needed for your specific setup.
That's it! You've successfully set up and used the Searcher project. Feel free to explore the different features and configurations based on your preferences and project requirements. If you encounter any issues or have specific tasks in mind, refer to the documentation or reach out for further assistance. Happy searching! 🚀

## Usage
Searcher offers a simple and intuitive interface for conducting privacy-respecting searches. Whether you're a first-time user or an experienced searcher, this guide will help you make the most out of your Searcher experience.

Accessing Searcher 
To access Searcher, open your web browser and navigate to the URL where your instance is hosted. If you've set up Searcher locally, the default URL is `http://127.0.0.1:8989`. If hosted remotely, replace the IP address and port with your server's information. 
$ xdg-open http://127.0.0.1:8989 # Replace with your actual URL 

Basic Search
Enter Your Query:
On the Searcher homepage, you'll find a search bar. Enter your query, whether it's a question, keyword, or phrase.
Press the "Enter" key or click the "Search" button to initiate the search.
Searcher will display relevant search results from various search engines in a clean and user-friendly format.

1.	Advanced Search Features
Searcher offers several advanced features to enhance your search experience:

Filters:
Refine your search using filters such as Images, Videos, News, and more. Explore the available filters to tailor your results.

Settings Menu:
Access the Settings menu to customize your Searcher instance. Here, you can adjust preferences, enable or disable plugins, and modify the appearance.

Keyboard Shortcuts:
Familiarize yourself with keyboard shortcuts for quicker navigation. For example, press g to focus on the search bar.

Image Search
Navigate to the Images Section:
Click on the "Images" tab to access the image search feature.

Enter Image Query:
Input your image-related query, whether it's a description or a specific keyword.

Review Image Results:
Searcher will display relevant images, allowing you to preview and explore without visiting external websites.

Privacy Tips
Use a VPN:
For an extra layer of privacy, consider using a Virtual Private Network (VPN) to obfuscate your IP address.

Review Settings:
Explore the Settings menu to review and adjust privacy-related configurations.

Troubleshooting
If you encounter any issues or have questions about using Searcher, refer to the Troubleshooting Guide for assistance. Additionally, engage with the community in the Discussions for support and feedback.
Now you're ready to make the most out of Searcher! Experiment with different queries, explore settings, and enjoy a privacy-respecting search experience.






## Customization
Searcher is designed with flexibility in mind, allowing users to customize various aspects of the search experience to suit individual preferences. This section outlines the key customization options available and how users can personalize their Searcher instance.

1.	Configuration Settings
The heart of Searcher's customization lies in its configuration settings. These settings are stored in the `settings.yml` file, located in the `/etc/searcher/` directory. To initiate customization:

  # Searcher settings

  use_default_settings: true

  general:
    debug: false
    instance_name: "Searcher"

  search:
    safe_search: 2
    autocomplete: 'duckduckgo'

  server:
    # Is overwritten by ${SEARXNG_SECRET}
    secret_key: "setsecretkey"
    limiter: true
    image_proxy: true
    # public URL of the instance, to ensure correct inbound links. Is overwritten
    # by ${SEARXNG_URL}.
    # base_url: http://example.com/location

  redis:
    # URL to connect redis database. Is overwritten by ${SEARXNG_REDIS_URL}.
    url: unix:///usr/local/searxng-redis/run/redis.sock?db=0

  ui:
    static_use_hash: true

  # preferences:
  #   lock:
  #     - autocomplete
  #     - method


enabled_plugins:
    - 'Hash plugin'
    - 'Self Informations'
    - 'Tracker URL remover'
    - 'Ahmia blacklist'
    # - 'Hostname replace'  # see hostname_replace configuration below
    # - 'Open Access DOI rewrite'

  # plugins:
  #   - only_show_green_results


 Use Default Settings

For a minimal setup, start with the default configuration provided. Copy the default settings file to the appropriate location:

$ sudo -H mkdir -p "/etc/ searcher "
$ sudo -H cp "/usr/local/searcher /searxng-src/utils/templates/etc/ searcher/settings.yml" \
             "/etc/ searcher /settings.yml"
This creates a baseline configuration that you can modify to match your preferences.

Modify Settings
Edit the /etc/searcher/settings.yml file to customize the behavior of your Searcher instance. Here are a few key settings you might want to adjust:
Instance Name: Change the instance_name field to give your instance a personalized name.
yaml
general: instance_name: "My Custom Searcher"

Search Preferences: Modify search-related settings such as safe_search and autocomplete according to your preferences.
search: safe_search: 2 autocomplete: 'duckduckgo' 

Server Configuration: Adjust server-related settings like secret_key, limiter, and image_proxy based on your security and privacy preferences.
server: secret_key: "your_secret_key" limiter: true image_proxy: true 

Restart Searcher
After modifying the configuration settings, restart your Searcher instance to apply the changes:
$ sudo systemctl restart searcher







2. User Interface Customization
Searcher provides a customizable user interface, allowing you to tweak the visual elements to enhance your search experience.

Custom CSS Styling
To add custom CSS styles to your Searcher instance, create a file named custom.css in the /usr/local/searcher/searxng-src/searx/static/css/ directory. This file will override the default styles.

/* Example custom.css content */ body { background-color: #f8f8f8; } /* Add your custom styles here */ 
Custom Logo and Favicon
Replace the default logo and favicon in the /usr/local/searxng/searxng-src/searx/static/img/ directory with your custom images. Ensure your custom logo is named searx.png and the favicon is named favicon.ico.

3. Plugin Management
Searcher supports plugins that extend its functionality. Customize your Searcher instance by enabling or disabling specific plugins. The enabled_plugins section in the settings.yml file controls this.
enabled_plugins: - 'Hash plugin' - 'Self Informations' - 'Tracker URL remover' - 'Ahmia blacklist' 

Enable or disable plugins based on your preferences and requirements.
















## Security Considerations
Ensuring the security and privacy of our users is a top priority for the Searcher project. By contributing to or using this software, it's important to be aware of certain security considerations and best practices.

Reporting Security Issues

If you discover any potential security vulnerabilities or issues, please report them responsibly. Follow these steps to report a security concern:

1. **Private Disclosure:**
   - Avoid disclosing security-related issues publicly.
   - Send an email to any of the contributors with a detailed description of the vulnerability.

2. **Include Information:**
   - Clearly outline the steps to reproduce the vulnerability.
   - Include information about the environment (e.g., operating system, browser, versions).

3. **Response Timeline:**
   - We are committed to responding promptly to security reports.
   - Initial acknowledgment within 48 hours, and we aim to provide a patch or resolution within 14 days.

Security Best Practices

When contributing code or utilizing the Searcher project, adhere to these security best practices:

1. **Code Review:**
   - All code changes undergo thorough review to identify potential security risks.
   - Collaborate with the community to ensure secure coding practices.

2. **Dependency Management:**
   - Regularly review and update project dependencies to patch known security vulnerabilities.
   - Avoid using outdated or unsupported libraries.

3. **Data Sanitization:**
   - Implement proper data sanitization techniques to prevent injection attacks.
   - Validate and sanitize user inputs before processing.

4. **Authentication and Authorization:**
   - Implement secure authentication mechanisms.
   - Enforce proper authorization checks to control access to sensitive functionalities.
5. **Secure Communication:**
   - Ensure that communication channels use secure protocols (e.g., HTTPS).
   - Protect sensitive data during transit by encrypting communications.

6. **Logging and Monitoring:**
   - Implement logging for security-relevant events.
   - Regularly monitor logs to detect and respond to suspicious activities.

7. **Privacy by Design:**
   - Consider user privacy in the design of new features.
   - Minimize data collection and storage to what is strictly necessary.

Code of Conduct

Security discussions and reports should adhere to our code of conduct. We strive to maintain a respectful and inclusive environment in addressing security matters.

Acknowledgments

We appreciate the efforts of the security community and individuals who responsibly disclose security issues. 

Thank you for prioritizing the security of Searcher and our users! 🛡️
















## Contributing
🎉 Thank you for considering contributing to the Searcher project! 🚀

We welcome contributions from the community to help improve and grow Searcher. Whether you're a developer, designer, tester, or documentation enthusiast, your efforts are highly valued.

Ways to Contribute

1. **Code Contributions:**
   - Fork the repository and create a branch for your contribution.
   - Make your changes, ensuring adherence to coding standards and conventions.
   - Submit a pull request with a clear description of your changes and their purpose.

2. **Bug Reporting:**
   - If you encounter a bug, please open a new issue.
   - Clearly describe the issue, including steps to reproduce it and the expected vs. actual behavior.
   - Provide relevant details such as your operating system, browser, and any error messages.

3. **Feature Requests:**
   - Suggest new features or improvements by opening an issue.
   - Clearly outline the proposed feature, its use case, and any potential implementation details.

4. **Documentation:**
   - Help improve the project's documentation by fixing typos, clarifying explanations, or adding missing information.
   - Documentation is located in the `/docs` directory.

5. **Testing:**
   - Test the project in different environments and report any compatibility issues.
   - Provide feedback on the user experience and suggest improvements.

Getting Started

1. **Set Up Your Development Environment:**
   - Fork the repository and clone it to your local machine.
   - Install the necessary dependencies following the instructions in the installation section.

2. **Branching Strategy:**
   - Create a new branch for each contribution to keep changes isolated.
   - Use meaningful branch names that describe the purpose of your changes.


3. **Coding Standards:**
   - Follow the coding standards and conventions outlined in the project.
   - Adhere to the existing code style to maintain consistency.

4. **Testing:**
   - Ensure that your changes are thoroughly tested before submitting a pull request.
   - Include relevant test cases for new features or bug fixes.

Code of Conduct

This project enforces a respectful and inclusive community. By participating, you are expected to uphold this code. Please report any unacceptable behavior.

Community Support

Join the community discussions in the [Discussions](https://github.com/deeze19/searcher/discussions) section. Share your ideas, ask questions, and collaborate with fellow contributors.

Attribution

All contributors will be acknowledged in the [Contributors](./CONTRIBUTORS.md) file. Your efforts are essential to the success of the Searcher project.

Thank you for making Searcher even better! 🌟















## License

Searcher Open-Source License (MIT)
Copyright © 2023 Deborah Ezekiel, Kenneth Burwell, and Oluwadara Dina for Searcher.
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

References

1. **SearXNG GitHub Repository:**
   - Original SearXNG project that Searcher is derived from.
   - [SearXNG GitHub](https://github.com/searxng/searxng)

2. **SearXNG Documentation:**
   - Official documentation for SearXNG, providing insights into its features and usage.
   - [SearXNG Documentation](https://searxng.github.io/searxng/)

3. **SearXNG Community Discussions:**
   - Join the community discussions around SearXNG for additional insights and support.
   - [SearXNG Discussions](https://github.com/searxng/searxng/discussions)
