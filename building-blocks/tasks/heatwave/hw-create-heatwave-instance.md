<!--
    {
        "name":"Create a Heatwave instance",
        "description":"Create a Heatwave instance in the private subnet"
    }
-->

Provision a Heatwave instance. 

1. Click the **Navigation menu** in the upper left, navigate to **Databases**, and under **HeatWave**, select **DB Systems**.
    
    ![Select HeatWave DB System](./images/20-select-heatwave-db-system.png "Select HeatWave DB System")

2. Ensure that **[](var:hw_compartment_name)** compartment is selected, and click **Create DB system**.

    ![Create DB system](./images/21-create-dbs.png "Create DB system")

3. In the **Create DB system** panel, select **Development or Testing**.

4. Under **Create in compartment**, ensure **[](var:hw_compartment_name)** is selected, and enter a name for the DB system, e.g. [](var:hw_dbs_name).

  **Name**:

    ```
    <copy> [](var:hw_dbs_name)</copy>
    ```

5. Enter the administrator credentials. *Note* the administrator credentials as you will need them to connect to the DB system. 

    ![HeatWave DB system details](./images/22-create-dbs-admin.png "HeatWave DB system details")

6. Select **Standalone** instance, and select the VCN, **[](var:hw_vcn_name)**, and private subnet, **private subnet-[](hw_vcn_name)**, which you created earlier.

   ![Configure networking](./images/23-configure-networking.png "Configure networking")

7. Let the **Configure placement** settings remain as is.

8. Under **Configure hardware**, select **Enable HeatWave cluster**, and click **Change shape**.

   ![Change shape](./images/24-change-shape.png "Change shape")

9. In the **Browse all shapes** page, ensure the compute model is **ECPU**, select **MySQL.32** shape, and click **Select a shape**. The ECPU Shape of the DB system must be MySQL.32.

    ![Select MySQL.32 shape](./images/25-select-mysql-32.png "Select MySQL.32 shape")

10. Click **Configure HeatWave cluster**.

    ![Configure HeatWave cluster](./images/26-configure-heatwave-cluster.png "Configure HeatWave cluster")

11. In **Configure HeatWave cluster** page, click **Change shape**.

    ![Change HeatWave shape](./images/27-change-heatwave-shape.png "Change Heatwave shape")

12. In the **Browse all shapes** page, select **HeatWave.512** shape, and click **Select a shape**. The HeatWave Shape must be HeatWave.512.

    ![Change HeatWave shape](./images/28-select-heatwave-512.png "Change Heatwave shape")

13. Select **HeatWave Lakehouse**, and click **Save changes**. HeatWave Lakehouse must be enabled on the DB system.

    ![Enable Lakehouse](./images/29-enable-lakehouse.png "Enable Lakehouse")

14. Click **Show advanced options**.

15. Go to the **Configuration** tab, and under **Database version**, select version **[](hw_db_version)** or higher version.

    ![Select database innovation version](./images/31-innovation-version.png "Select database innovation version")

16. Go to the **Connections** tab, enter the **Hostname**, which is same as DB system name e.g. [](hw_db_name), and click **Create**:

    **Hostname**:

    ```
    <copy>heatwave-genai-dbs</copy>
    ```

    ![HeatWave hostname](./images/32-heatwave-hostname.png "HeatWave hostname")

17.  While the DB system is created, the state is shown as **CREATING**.

    ![Show creating state](./images/33-dbs-creating.png "Show creating state")

18. The new DB system will be ready to use after a few minutes. The state **ACTIVE** indicates that the DB system is ready for use. 

    ![Show active state](./images/34-dbs-active.png "Show active state")

19. In the **Connections** tab, note the **Private IP address** of the DB system, which is the HeatWave endpoint.

    ![Heatwave endpoint](./images/35-heatwave-endpoint.png "Heatwave endpoint")