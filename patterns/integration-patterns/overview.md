---
title: Overview
---


# Patterns from *Enterprise Integration Patterns* by Gregor Hohpe and Bobby Woolf

Below is a bullet list of the 65 patterns from *Enterprise Integration Patterns: Designing, Building, and Deploying Messaging Solutions* by Gregor Hohpe and Bobby Woolf (2003). Each pattern includes its name and a brief description of its purpose, focusing on solutions for enterprise application integration using messaging.[](https://en.wikipedia.org/wiki/Enterprise_Integration_Patterns)

- **Aggregator**: Combines multiple related messages into a single message based on a correlation strategy, enabling processing of aggregated data.
- **Canonical Data Model**: Defines a standard data format for messages to ensure consistency across different systems, reducing transformation complexity.
- **Channel Adapter**: Connects an application to a messaging system by adapting its API to the messaging infrastructure, enabling seamless integration.
- **Channel Purger**: Removes all messages from a channel for testing or cleanup, ensuring a clean slate for message processing.
- **Claim Check**: Stores large message payloads in a persistent store and sends a reference (claim check) in the message, reducing message size.
- **Command Message**: Represents a command to invoke a specific operation on a receiver, enabling remote procedure calls via messaging.
- **Competing Consumers**: Allows multiple consumers to process messages from a single queue concurrently, improving throughput and scalability.
- **Content Enricher**: Adds missing data to a message by retrieving it from an external source, ensuring the message contains all required information.
- **Content Filter**: Removes unnecessary or sensitive data from a message, reducing its size and simplifying downstream processing.
- **Content-Based Router**: Routes a message to different youre a destination based on its content, enabling dynamic message routing.
- **Control Bus**: Uses a dedicated channel to send control messages that manage or monitor the messaging system, ensuring operational control.
- **Correlation Identifier**: Assigns a unique ID to a message to track related messages across multiple channels or systems, enabling message correlation.
- **Databank Channel**: Stores messages in a database-like channel for later retrieval, supporting asynchronous or delayed processing.
- **Dead Letter Channel**: Sends undeliverable or unprocessed messages to a special channel for error handling or manual inspection.
- **Document Message**: Represents a document (data) without specific processing instructions, allowing flexible handling by the receiver.
- **Durable Subscriber**: Ensures a subscriber receives all messages, even those sent while disconnected, by storing them until delivery.
- **Dynamic Router**: Routes messages to destinations based on dynamically updated routing rules, providing flexible routing logic.
- **Envelope Wrapper**: Wraps a message in an envelope with additional metadata (e.g., headers), enabling standardized message handling.
- **Event Message**: Notifies subscribers of an event without expecting a response, enabling decoupled event-driven communication.
- **Event-Driven Consumer**: Triggers message processing when a message arrives, eliminating the need for polling and improving responsiveness.
- **File Transfer**: Moves files between systems without using messaging channels, providing a simple integration method for file-based systems.
- **Filter**: Discards messages that don’t meet specific criteria, preventing unnecessary processing by downstream components.
- **Format Indicator**: Includes metadata to indicate the message’s data format, enabling correct interpretation by the receiver.
- **Guaranteed Delivery**: Ensures messages are delivered despite failures by using persistent storage and retry mechanisms.
- **Idempotent Receiver**: Ignores duplicate messages to prevent reprocessing, ensuring safe message handling in unreliable systems.
- **Message**: Encapsulates data and metadata for transmission between systems, enabling standardized communication.
- **Message Bus**: Transports messages between multiple components or applications, acting as a central communication backbone.
- **Message Channel**: Connects a sender and receiver for message exchange, providing a conduit for asynchronous communication.
- **Message Dispatcher**: Routes messages from a single channel to multiple consumers based on workload, enabling load balancing.
- **Message Endpoint**: Connects an application to a messaging system as a sender or receiver, facilitating integration.
- **Message Expiration**: Sets a time limit for a message’s validity, discarding it if undelivered or unprocessed in time.
- **Message Filter**: Filters messages based on criteria, allowing only relevant messages to proceed to the receiver.
- **Message History**: Attaches a history of processing steps to a message, enabling tracking and debugging of message flow.
- **Message Sequence**: Ensures messages are processed in a specific order by using sequence identifiers, maintaining logical order.
- **Message Store**: Persists messages in a database for auditing, recovery, or delayed processing, ensuring reliability.
- **Message Translator**: Converts a message’s format or structure to match the receiver’s requirements, enabling interoperability.
- **Messaging Bridge**: Connects two different messaging systems, allowing messages to flow between disparate platforms.
- **Messaging Gateway**: Encapsulates messaging system access within an application, simplifying interaction with the messaging infrastructure.
- **Normaliser**: Transforms messages of different formats into a common format, simplifying downstream processing.
- **Pipes and Filters**: Breaks down message processing into a series of independent filter components connected by pipes, enabling modular processing.
- **Point-to-Point Channel**: Delivers a message to a single receiver, ensuring direct and exclusive communication.
- **Polling Consumer**: Periodically checks a channel for new messages, enabling message retrieval in systems without event-driven support.
- **Process Manager**: Orchestrates a multi-step process by routing messages between components, managing complex workflows.
- **Publish-Subscribe Channel**: Broadcasts a message to all subscribers of a channel, enabling one-to-many communication.
- **Recipient List**: Sends a message to a dynamically determined list of recipients, enabling flexible multicast distribution.
- **Request-Reply**: Sends a request message and expects a reply, enabling synchronous-like communication over asynchronous messaging.
- **Resequencer**: Reorders messages that arrive out of sequence, ensuring they are processed in the correct order.
- **Return Address**: Specifies the reply channel in a request message, directing where the response should be sent.
- **Routing Slip**: Attaches a predefined list of processing steps to a message, guiding it through a specific sequence of components.
- **Scatter-Gather**: Sends a message to multiple recipients and aggregates their responses into a single result, enabling parallel processing.
- **Selective Consumer**: Filters messages to process only those meeting specific criteria, reducing unnecessary processing.
- **Service Activator**: Triggers a service or application in response to a message, connecting messaging to business logic.
- **Shared Database**: Enables integration by having multiple applications access a common database, simplifying data sharing.
- **Smart Proxy**: Intercepts messages to monitor or modify their flow without altering the core messaging system, enabling tracking or control.
- **Splitter**: Breaks a composite message into individual messages for separate processing, enabling fine-grained handling.
- **Test Message**: Sends a test message through the system to verify functionality or diagnose issues, ensuring system reliability.
- **Transactional Client**: Ensures message sending or receiving is part of a transaction, guaranteeing atomicity and consistency.
- **Wire Tap**: Copies messages to a secondary channel for monitoring or auditing without affecting the primary flow, enabling observability.
