# Oracle TNS

What is Oracle TNS?

Oracle TNS (Transparent Network Substrate) is a communication protocol used by Oracle databases to facilitate connections between clients and servers. It is widely used in enterprise environments such as healthcare, finance, and retail due to its robust features:

Supports encryption of communications;
Operates over multiple network protocols (TCP/IP, UDP, etc.);
Enables load management, connection balancing, logging, and monitoring.


Default Behavior

By default, TNS listens on TCP port 1521.
Configuration is managed through the following files:
**tnsnames.ora** – client-side file defining how the client connects to the database;
**listener.ora** – server-side file defining what the Oracle listener accepts and how it handles connections.

<img width="824" height="402" alt="image" src="https://github.com/user-attachments/assets/5eb81f37-f209-4615-ad5d-02e03e6fdd46" />

We use sqlplus to interact with Oracle databases via the command line. It allows us to authenticate, execute SQL queries, run scripts, and administer the database directly.

<img width="921" height="748" alt="image" src="https://github.com/user-attachments/assets/03d66b2f-9bf6-4617-ac90-ebad14d4459f" />

<img width="713" height="948" alt="image" src="https://github.com/user-attachments/assets/583e387c-609f-468f-99fd-6e5baed2bddf" />
