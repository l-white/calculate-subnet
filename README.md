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

## Requirements

Document your solution with the following details for each server category:

- Server category name
- Required number of IP addresses (considering future growth)
- Subnet mask
- Network address
- Range of usable IP addresses

## Solution

### 1. Calculate the number of required IP addresses for each server
- Web Servers: 75
- Database Servers: 45
- Application Servers: 60

### 2. Determine the subnet mask
We need a minimum of 75 hosts per subnet, and since this falls between 64 and 128, we need 7 bits for the hosts and 1 for the network.
2**7 = 128

To determine the subnet, we need to convert the host portion to binary: 10.10.00000000.0 | 0000000 --> Subnet is 25 (8 bits + 8 bits + 9 bits) and host is 7 bits (32-25=7)

Subnet mask: 255.255.255.128/25

### 3. Calculate the network address and the range of usable IP addresses for each subnet

- 1st subnet: 10.0.0.00000000.0 | 0000000 = 10.0.0.0/25
- 2nd subnet: 10.0.0.00000000.1 | 0000000 = 10.0.0.128/25
- 3rd subnet: 10.0.0.00000001.0 | 0000000 = 10.0.0.0/25

#### Web Servers
- **Network:** 10.0.0.0
- **1st Host:** 10.0.0.1
- **Last Host:** 10.0.0.126
- **Broadcast Address:** 10.0.0.127

#### Database Servers
- **Network:** 10.0.0.128
- **1st Host:** 10.0.0.129
- **Last Host:** 10.0.0.254
- **Broadcast Address:** 10.0.0.255

#### Application Servers
- **Network:** 10.0.1.0
- **1st Host:** 10.0.1.1
- **Last Host:** 10.0.1.126
- **Broadcast Address:** 10.0.1.127
