<!--
    {
        "name":"Allow incoming connections for the compute",
        "description":"Update the VCN security list to allow HTTP connections"
    }
-->

Update the security list for the public network to allow HTTP connections.

1. Click the **Navigation menu** in the upper left, navigate to **Networking**, and select **Virtual cloud networks**.

    ![Select VCN](./images/3-select-vcn.png "Select VCN")

2. Under **Compartment**, ensure **[](var:hw_compartment_name)** is selected, and click the VCN you created, **[](var:hw_vcn_name)**.

    ![Select VCN](./images/14-select-vcn.png "Select VCN")

3. On the **[](var:hw_vcn_name)** page, under **Subnets**, click  **public subnet-[](var:hw_vcn_name)**.

    ![Select public subnet](./images/15-public-subnet.png "Select public subnet")

4. Click **Default Security List for [](var:hw_vcn_name)**.

    ![Default security list](./images/16-default-security-list.png "Default security list")

5. On **Default Security List for [](var:hw_vcn_name)** page, under **Ingress Rules**, click **Add Ingress Rules**.

    ![Add ingress rules in default security list](./images/17-add-ingress-rules-default-security-list.png "Add ingress rules in default security list")

6. On **Add Ingress Rules** panel, enter the following, and click **Add Ingress Rules**:

    **Source CIDR**:

    ```
    <copy>0.0.0.0/0</copy>
    ```

    **Destination Port Range**:

    ```
    <copy>80,443</copy>
    ```

    ![Ingress rules](./images/18-enter-ingess-rules-default-security-list.png "Ingress rules") 

7. On **Default Security List for [](var:hw_vcn_name)** page, the new ingress rules are shown under **Ingress Rules**.

    ![New ingress rules](./images/19-new-ingress-rules-default-security-list.png "New ingress rules")