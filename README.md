# IP Addressing Strategy

## Scenario

You are the network administrator for a large company with the following services hosted on various servers:

- **Web Servers**: 50 servers
- **Database Servers**: 30 servers
- **Application Servers**: 40 servers

The company has been assigned the IP address range `10.0.0.0/22`. You need to create a subnet plan that allocates IP addresses to each type of server while maximizing the efficient use of addresses and ensuring security and manageability.

## Requirements

1. Each type of server must have its own subnet.
2. Use a single subnet mask for all categories.
3. Consider potential future growth (up to 50% increase in the number of servers) in each category when planning the subnets.
4. Determine the subnet mask, network address, and the range of usable IP addresses for each subnet.

## Task

1. **Subnet Calculation:**
   - Calculate the required number of IP addresses for each server category, considering future growth.
   - Determine a single subnet mask that can be used for all server categories.
   - Calculate the network address and the range of usable IP addresses for each subnet.

2. **Address Allocation:**
   - Allocate IP addresses to each server category based on the calculated subnets.

## Solution

Document your solution with the following details for each server category:

- Server category name
- Required number of IP addresses (considering future growth)
- Subnet mask
- Network address
- Range of usable IP addresses
