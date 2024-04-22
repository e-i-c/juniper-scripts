
# L3VPN Provisioning for Juniper MX-Series Devices

*README.md*

The purpose of the script, “L3VPN_config_script”, is to generate configurations for provisioning new L3VPN connections between a Provider Edge (PE) and Customer Edge (CE) router.

This script is targeted towards individuals that do not have the ability to utilize third-party APIs or network automation suites in their environment, and need something simple and reliable to generate L3VPN configurations for Juniper MX-series devices.




## Valid Equipment

These configurations are specifically meant to be deployed to Juniper MX-series devices, and has been tested and validated on the following devices:
- Juniper MX104
- Juniper MX204
- Juniper MX240
- Juniper MX480
## Acknowledgements
Additional resources for creating L3VPN connections on Juniper devices can be found at the following links:

 - [Configure a Basic MPLS-Based Layer 3 VPN](https://www.juniper.net/documentation/us/en/software/junos/vpn-l3/topics/example/mpls-qfx-series-vpn-layer3.html)
 - [Routing Instances in Layer 3 VPNs](https://www.juniper.net/documentation/us/en/software/junos/vpn-l3/topics/topic-map/l3-vpns-routing-instances.html)
 - [IPv4 Traffic Over Layer 3 VPNs](https://www.juniper.net/documentation/us/en/software/junos/vpn-l3/topics/topic-map/l3-vpns-ipv4-traffic.html)
 - [Configuring an AS for Layer 3 VPNs](https://www.juniper.net/documentation/us/en/software/junos/vpn-l3/topics/topic-map/l3-vpns-as-configuration.html)


## Deployment

To deploy this project, first ensure you have the L3VPN_config_script.exe file installed. Simply open the file from its icon. Then, follow the prompt to fill out the information for the desired L3VPN service. 

Once prompted, if all of the information is correct, generate the configuration. Then, copy and paste the configuration lines into a Juniper MX-series router in 'configuration' mode. You may also enter 'show | compare' to see the changes made and verify that they are correct. If correct, enter a 'commit' to save the configurations. 

Once the CE side is also built, you may verify the peering is established by running the following command:

show bgp summary instance *'your VPN name here'*

If configuration was done correctly, you will see the BGP peer 'Established'.


## Documentation

[Final Project Documentation](https://github.com/e-i-c/juniper-scripts/blob/main/Final%20Project%20Documentation.docx)


## Authors

- [@e-i-c](https://github.com/e-i-c)



