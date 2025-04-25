# Intelligent Assistant for Chevrolet Dealership

## Description

This project is an intelligent assistant designed for a Chevrolet dealership, aimed at optimizing customer management, inventory, and service appointments. It leverages artificial intelligence and integrates with Google and Supabase tools to enhance operational efficiency and improve the customer experience.

---

## Workflow Overview of How Components Work

The workflow of the assistant integrates various components to handle tasks such as customer inquiries, service appointments, and inventory management. Here’s a step-by-step overview of how the components interact in a typical workflow:

1. **Customer Interaction**: The customer sends a message via WhatsApp, which triggers the assistant using the WhatsApp Trigger component. The assistant responds through the OpenAI Chat Model to engage in conversation.

2. **Request Handling**: Based on the customer's inquiry, the Switch component directs the request to the appropriate function, such as checking available vehicles or scheduling a service appointment.

3. **Service Scheduling**: If the customer wants to book a service appointment, the assistant checks the Google Calendar (using the Read Calendar component) for availability. It can also create, update, or delete calendar events as needed using the Create, Update, or Delete Calendar components.

4. **Inventory Management**: For inquiries about vehicle availability, the assistant can access Google Sheets (using Google Sheets Read) to retrieve the latest inventory data. It can also add new vehicles or update existing inventory entries with Google Sheets Add Rows or Update Rows.

5. **Personalized Experience**: Throughout the conversation, the Simple Memory component stores relevant information, allowing the assistant to provide a personalized experience by remembering past interactions.

6. **Notifications**: Once an appointment is confirmed, the assistant sends a notification to the customer via WhatsApp Business. If required, it may also send follow-up emails or confirmations using Gmail.

7. **Search Functionality**: For more complex queries or searches, the Supabase Vector Store and OpenAI Embeddings are used to enable semantic search, allowing the assistant to provide more accurate and relevant results related to vehicles and services.

---

## Deep Dive into Components

### 1. WhatsApp Trigger
- The **WhatsApp Trigger** is the first point of contact for the customer. When a user sends a message to the dealership’s WhatsApp Business number, it triggers the assistant’s workflow. The assistant can respond to queries, initiate actions like scheduling appointments, or guide users to the right service.

### 2. Switch
- The **Switch** component is responsible for routing requests. It acts as a decision point in the workflow, ensuring that each query is handled by the correct component. If a customer asks about available vehicles, for example, the request will be forwarded to the inventory management system; if they inquire about service appointments, it will route the request to the calendar and appointment scheduling components.

### 3. AI Agent
- The **AI Agent** plays the role of the core brain of the assistant. It leverages machine learning algorithms to understand and interpret the customer’s intent based on the query and interacts with the appropriate components to provide a response or take action.

### 4. OpenAI Chat Model
- The **OpenAI Chat Model** powers the conversational aspect of the assistant. It is designed to handle natural language processing (NLP) tasks, ensuring smooth and meaningful interactions. It can respond to customer inquiries, explain product features, or guide users through the dealership’s offerings.

### 5. Google Sheets Integration
- The **Google Sheets Read** and **Google Sheets Add/Update Rows** components integrate with Google Sheets to provide real-time access to the dealership's data, such as vehicle inventory or customer information. This integration ensures that the assistant can keep data up to date and respond accurately to customer inquiries regarding product availability, pricing, and more.

### 6. Calendar Management
- The **Calendar** components (Read, Create, Update, and Delete) integrate with Google Calendar, making it easy for the assistant to manage service appointments. Customers can schedule, modify, or cancel appointments directly through the assistant, which will update the dealership's calendar accordingly.

### 7. Notifications
- The **WhatsApp Business** and **Gmail** components send notifications and confirmations to customers. Once a customer books a service or test drive, the assistant sends confirmation messages through WhatsApp or email, ensuring that the customer is always informed about the status of their appointment.

---

This detailed breakdown of the workflow and components ensures that all tasks are automated and optimized, improving both operational efficiency and customer satisfaction.

