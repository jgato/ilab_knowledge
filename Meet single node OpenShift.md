# Meet single node OpenShift: Our newest small OpenShift footprint for edge architectures 

The cloud native approach to developing and deploying applications is increasingly being adopted in the context of edge computing. However, edge workloads and use cases span a myriad of locations, technical requirements, and physical footprints. 

At Red Hat, we are seeing an emerging pattern in which some infrastructure providers and application owners want a consistent workload life cycle approach across the business. This includes their on-premises, hybrid/multicloud, and edge architectures as well as continuous operations and management of sites that might have intermittent or very low bandwidth connectivity back to a central site.

For example, think of locations such as cruise ships that spend some of their time docked and directly connected to a regional data center, while other times they are out at sea with a slow, high-latency satellite connection. 

We also observed that in these remote locations, as the distance between an edge site and the central management hub grows, the physical space for systems decreases. This means these edge locations operate with very limited space as well as power and cooling, creating an environment suited for a single server. 

## Introducing Red Hat OpenShift in a single node 

Until today the smallest supported cluster size (including control and worker nodes) was the three node cluster. As of OpenShift 4.9, we now have a full OpenShift deployment in a single node. This fully supported topology joins the three node cluster and remote worker topologies to offer three options to meet more customer requirements in more edge environments. Single node OpenShift offers both control and worker node capabilities in a single server and provides users with a consistent experience across the sites where OpenShift is deployed, regardless of the size of the deployment.

Because a single node offers both control and worker node functionality, users who have adopted Kubernetes at their central management sites and who wish to have independent Kubernetes clusters at edge sites can deploy this smaller OpenShift footprint and have minimal to no dependence on the centralized management cluster and can run autonomously when needed.

Just like multi node OpenShift, the single node deployment extends the OpenShift experience, taking advantage of the same skills and tools and bringing consistent upgrades and life cycle management throughout the container stack, including the operating system, feature-rich Kubernetes (including cluster services), and applications.

Keep in mind a single node OpenShift deployment differs from the default self-managed/highly-available cluster profile in couple of ways:

 * To optimize system resource usage, many operators are configured to reduce the footprint of their operands when running on a single node OpenShift.
 * In environments that require high availability, it is recommended that the architecture be configured in a way in which if the hardware was to fail, those workloads are transitioned to other sites or nodes while the impacted node is recovered. 

## Think cell towers, not data centers

Single node OpenShift focuses on reducing the prerequisites for OpenShift deployment on bare metal nodes, bringing the barrier to entry down to a minimum, further simplifying and streamlining the deployment experience of OpenShift. This is especially useful when deploying environments that need to occupy the absolute smallest footprint and have minimum external requirements.

One example of this use case is seen in telecommunication service providers' implementation of a Radio Access Network (RAN) as part of a 5G mobile network.
In the context of telecommunications service providers' 5G RANs, it is increasingly common to see "cloud native" implementations of the 5G Distributed Unit (DU) components. Due to latency constraints, the DU needs to be deployed very close to the Radio Units (RUs), for which it is responsible. In practice, this can mean running the DU on anything from a single server at the base of a cell tower to a more datacenter-like environment serving several RUs.

A typical DU example is a resource-intensive workload, requiring 6 dedicated cores per DU and several DUs packed on the server, with 16-24 GB of RAM per DU (consumed as huge pages), multiple single route I/O virtualization (SR-IOV) NICs, FPGA, or GPU acceleration cards  carrying several Gbps of traffic each.

One crucial detail of this use case is ensuring that this workload can be "autonomous" so that it can continue operating with its existing configuration, even when any centralized management functionality is unavailable. This is where single node OpenShift comes in.

author: Moran Goldboim, Eran Cohen
