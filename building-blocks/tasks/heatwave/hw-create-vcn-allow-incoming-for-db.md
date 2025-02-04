<!--
    {
        "name":"Allow incoming connections for the database",
        "description":"Update the VCN security list to allow connections to the database on specific ports"
    }
-->

We will update the security lists to add ingress rules for connecting to the database instance. 

1. On the **[](var:hw_vcn_name)** page, under **Subnets**, click  **private subnet-[](var:hw_vcn_name)**.

     ![Show subnet details](./images/9-heatwave-genai-vcn-subnets.png "Show subnet details")

2. On **private subnet-[](var:hw_vcn_name)** page, under **Security Lists**, click  **security List for private subnet-[](var:hw_vcn_name)**.

    ![Select security lists](./images/10-select-security-list.png "Select security lists")

3. On the **security list for private subnet-[](var:hw_vcn_name)** page, under **Ingress Rules**, click **Add Ingress Rules**.

    ![Add ingress rules](./images/11-add-ingress-rules.png "Add ingress rules")

4. On **Add Ingress Rules** panel, enter the following, and click **Add Ingress Rules**:

    **Source CIDR**:

    ```
    <copy>0.0.0.0/0</copy>
    ```

    **Destination Port Range**:

    ```
    <copy>3306,33060</copy>
    ```

    ![Ingress rules](./images/12-enter-ingress-rules.png "Ingress rules")

5. On **security list for private subnet-[](var:hw_vcn_name)** page, the new ingress rules are shown under **Ingress Rules**.

    ![New ingress rules](./images/13-new-ingress-rules.png "New ingress rules")
