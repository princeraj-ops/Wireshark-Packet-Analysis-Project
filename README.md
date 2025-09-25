# Wireshark Project: Packet Capture and Analysis

## Summary

This project demonstrates the use of Wireshark to capture, filter, and analyze network traffic. The primary objectives included capturing live packets, using display filters to isolate specific protocols (HTTP and HTTPS), detecting IP addresses, and combining filters to exclude specific traffic from a capture.

## Tools Used

* **Wireshark:** For packet capture and analysis.
* **Firefox Browser:** To generate network traffic for analysis.

## Project Walkthrough

This project was completed by performing a series of structured tasks to demonstrate core Wireshark functionalities.

### Task 1: Basic HTTP Packet Filtering

* **Objective:** Use Wireshark to capture packets and apply a filter to display only HTTP packets.
* **Process:**
    1.  [cite_start]Started a live packet capture on the ethernet network[cite: 5].
    2.  [cite_start]Visited the non-secure URL `http://cygwin.com` to generate HTTP traffic[cite: 5].
    3.  [cite_start]Stopped the capture and saved the file[cite: 5].
    4.  [cite_start]Applied a display filter for port 80 to isolate the HTTP packets[cite: 5].

    *Screenshot of the port 80 filter results:*
    `<img width="997" height="602" alt="Screenshot 2025-09-25 at 1 28 44 AM" src="https://github.com/user-attachments/assets/9d1ea4b0-084b-4b49-b5f8-1896b752b3ca" />`

### Task 2: Advanced Filtering with Logical Operators

* [cite_start]**Objective:** To capture traffic from multiple sites and use logical operators (OR, AND) to filter for specific HTTP and HTTPS packets while excluding a known IP address[cite: 1, 2].
* **Process:**
    1.  [cite_start]Cleared the browser cache and began a new packet capture in Wireshark[cite: 2].
    2.  [cite_start]Generated traffic by visiting Google.com, duckduckgo.com (HTTPS), and http://cygwin.com (HTTP)[cite: 2].
    3.  [cite_start]**Detected IP Address [cite: 3][cite_start]:** First, I isolated the traffic for the non-secure Cygwin site by filtering for TCP port 80 to identify its IP address[cite: 2].

        *Screenshot of identifying the Cygwin IP address:*
        `<img width="999" height="609" alt="identifying_ip" src="https://github.com/user-attachments/assets/69621993-a7af-47d3-9b5e-26460ab88ad6" />`

    4.  [cite_start]**Filtered for HTTP and HTTPS [cite: 6][cite_start]:** Next, I created a display filter to show all HTTP and HTTPS packets using an OR condition[cite: 2].

        *Screenshot of the combined HTTP/HTTPS filter:*
        `<img width="997" height="604" alt="http:https_packet" src="https://github.com/user-attachments/assets/9fedd566-6f82-41d0-8eb5-e8ff16590806" />
`

    5.  [cite_start]**Excluded Specific IP Address [cite: 1][cite_start]:** Finally, I modified the filter using an AND condition to eliminate all packets from the previously identified Cygwin IP address, successfully isolating only the HTTPS traffic from the other sites[cite: 2].

        *Screenshot of the final filter excluding the Cygwin IP:*
        `<img width="1000" height="609" alt="excluding_ip" src="https://github.com/user-attachments/assets/4212c542-5ec4-441a-b0f7-678ab152c840" />
`

## Conclusion

This project provided hands-on experience with the fundamental features of Wireshark. Key skills demonstrated include:
* [cite_start]Starting and saving a live packet capture[cite: 4].
* [cite_start]Using display filters to detect both HTTPS and HTTP packets[cite: 6, 5].
* [cite_start]Isolating traffic to find the IP address of a specific web page[cite: 3].
* Applying logical operators like AND and OR to create complex and specific display filters.

This exercise was a practical demonstration of how a security analyst can use Wireshark to narrow down vast amounts of network data to investigate specific events or traffic.
