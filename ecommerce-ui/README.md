**🛍️ E-commerce UI**

This Docker image provides a React application with a Node.js server for an e-commerce user interface. The application connects to six different microservices to provide the optimal e-commerce experience.

**✨ Summary**

Looking to make an impact in the world of e-commerce? This project offers a chance to demonstrate your proficiency in modern web development, containerization, and microservices architecture. Dive in to learn, contribute, and enhance your portfolio with a real-world application that is both complex and rewarding.

**🚀 Prerequisites**

Before running a container from this image, ensure that you have the following:

🐳 Docker installed on your system
🔗 Access to the six microservices required by the application


**🏃 Usage**

To run a container from this image, use the following command:

'' bash -- Copy code
docker run --network=my-network -p 4000:4000 \
-e REACT_APP_PROFILE_API_HOST=http://profile-management \
-e REACT_APP_PRODUCT_API_HOST=http://product-catalog \
-e REACT_APP_INVENTORY_API_HOST=http://product-inventory \
-e REACT_APP_ORDER_API_HOST=http://order-management \
-e REACT_APP_SHIPPING_API_HOST=http://shipping-and-handling \
-e REACT_APP_CONTACT_API_HOST=http://contact-support-team \
--name ecommerce-ui rslim087/ecommerce-ui

Replace my-network with the name of the Docker network where the required microservices are running. The container exposes port 4000, which you can map to a desired port on your host machine using the -p flag.

**🔧 Environment Variables**

The container requires the following environment variables to be set:

REACT_APP_PROFILE_API_HOST: The URL of the profile management microservice.
REACT_APP_PRODUCT_API_HOST: The URL of the product catalog microservice.
REACT_APP_INVENTORY_API_HOST: The URL of the product inventory microservice.
REACT_APP_ORDER_API_HOST: The URL of the order management microservice.
REACT_APP_SHIPPING_API_HOST: The URL of the shipping and handling microservice.
REACT_APP_CONTACT_API_HOST: The URL of the contact support team microservice.
The application uses the provided environment variables to construct the full URL for making requests to the respective microservices. Each variable should be set to the scheme and hostname of the corresponding service, such as REACT_APP_PROFILE_API_HOST=http://profile-management. The application will then append the appropriate port and path, like :3003/api/update, to complete the URL and send the request to the specified microservice container.

**🌐 Docker Network**

The e-commerce UI container needs to be connected to the same Docker network as the microservices it depends on. You can achieve this in two ways:

By specifying the --network flag when running the container, as shown in the usage example above. Ensure that the microservices are also running on the same network specified.

By using Docker Compose to define and run the e-commerce UI container along with the microservices. In this case, you can define a common network in the Docker Compose file and connect all the containers to that network.

**🛠️ Building the Image**

If you want to build the Docker image yourself, follow these steps:

Clone the repository containing the application code.

Navigate to the directory where the Dockerfile is located.

Run the following command to build the image:

bash
Copy code
docker build -t rslim087/ecommerce-ui .
This command will build the Docker image using the provided Dockerfile and tag it as rslim087/ecommerce-ui.

**🤝 Contributing**

If you would like to contribute to this project, please follow the guidelines in the CONTRIBUTING.md file.

**📄 License**

This project is licensed under the MIT License.

**🛠️ Support**

If you encounter any issues or have questions regarding this Docker image or the e-commerce UI application, please open an issue on the GitHub repository.

Feel free to customize this README according to your specific project details and requirements.
