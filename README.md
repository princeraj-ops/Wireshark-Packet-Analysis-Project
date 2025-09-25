# Wireshark Project: Packet Capture and Analysis

## Summary

This project demonstrates the use of Wireshark to capture, filter, and analyze network traffic. The primary objectives included capturing live packets, using display filters to isolate specific protocols (HTTP and HTTPS), detecting IP addresses, and combining filters to exclude specific traffic from a capture.

## Tools Used

* **Wireshark:** For packet capture and analysis.
* **Firefox Browser:** To generate network traffic for analysis.

***

## Project Walkthrough

This project was completed by performing a series of structured tasks to demonstrate core Wireshark functionalities.

### Task 1: Basic HTTP Packet Filtering

* **Objective:** Use Wireshark to capture packets and apply a filter to display only HTTP packets.
* **Process:**
    1.  Started a live packet capture on the ethernet network.
    2.  Visited the non-secure URL `http://cygwin.com` to generate HTTP traffic.
    3.  Stopped the capture and saved the file.
    4.  Applied a display filter for port 80 to isolate the HTTP packets.

    *Screenshot of the port 80 filter results:*
    ![Screenshot of HTTP filter results](https://github.com/user-attachments/assets/9d1ea4b0-084b-4b49-b5f8-1896b752b3ca)

### Task 2: Advanced Filtering with Logical Operators

* **Objective:** To capture traffic from multiple sites and use logical operators (OR, AND) to filter for specific HTTP and HTTPS packets while excluding a known IP address.
* **Process:**
    1.  Cleared the browser cache and began a new packet capture in Wireshark.
    2.  Generated traffic by visiting Google.com, duckduckgo.com (HTTPS), and http://cygwin.com (HTTP).
    3.  **Detected IP Address:** First, I isolated the traffic for the non-secure Cygwin site by filtering for TCP port 80 to identify its IP address.

        *Screenshot of identifying the Cygwin IP address:*
        ![Screenshot of identifying the Cygwin IP address](https://github.com/user-attachments/assets/69621993-a7af-47d3-9b5e-26460ab88ad6)

    4.  **Filtered for HTTP and HTTPS:** Next, I created a display filter to show all HTTP and HTTPS packets using an OR condition.

        *Screenshot of the combined HTTP/HTTPS filter:*
        ![Screenshot of combined HTTP and HTTPS packets](https://github.com/user-attachments/assets/9fedd566-6f82-41d0-8eb5-e8ff16590806)

    5.  **Excluded Specific IP Address:** Finally, I modified the filter using an AND condition to eliminate all packets from the previously identified Cygwin IP address, successfully isolating only the HTTPS traffic from the other sites.

        *Screenshot of the final filter excluding the Cygwin IP:*
        ![Screenshot of final filter excluding the Cygwin IP](https://github.com/user-attachments/assets/4212c542-5ec4-441a-b0f7-678ab152c840)

***

## Conclusion

This project provided hands-on experience with the fundamental features of Wireshark. Key skills demonstrated include:
* Starting and saving a live packet capture.
* Using display filters to detect both HTTPS and HTTP packets.
* Isolating traffic to find the IP address of a specific web page.
* Applying logical operators like AND and OR to create complex and specific display filters.

This exercise was a practical demonstration of how a security analyst can use Wireshark to narrow down vast amounts of network data to investigate specific events or traffic.
## Certifications

* [Wireshark for Beginners: Capture Packets](https://coursera.org/verify/DJDYRPI2Q0D5) - Coursera Project Network, Sep 2025 
