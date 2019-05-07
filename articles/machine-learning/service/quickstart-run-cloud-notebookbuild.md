# Quickstart: Use a cloud-based notebook server to get started with Azure Machine Learning

Create a cloud-based notebook server, then use it.  In this quickstart, you run Python code that logs values in the Azure Machine Learning service workspace. The workspace is the foundational block in the cloud that you use to experiment, train, and deploy machine learning models with Machine Learning. 

This quickstart shows how to create a cloud resource in your Azure Machine Learning workspace, configured with the Python environment necessary to run Azure Machine Learning.
 
In this quickstart, you take the following actions:

* Create a new cloud-based notebook server in your workspace
* Launch the Jupyter web interface
* Open a notebook that contains code to estimate pi and logs errors at each iteration.
* Run the notebook.
* View the logged error values in your workspace.  This example shows how the workspace can help you keep track of information generated in a script. 

## Use an existing Machine Learning Service Workspace Resource in Azure
In this quickstart, use a Machine Learning Service Workspace resource created for you, found in the [Azure Portal](https://ms.portal.azure.com/). 

## Create a cloud-based notebook server

 From your workspace, you create a cloud resource to get started using Jupyter notebooks. This resource gives you a cloud-based platform pre-configured with everything you need to run Azure Machine Learning service.

1. Open your workspace in the [Azure portal](https://portal.azure.com/).

1. On your workspace page in the Azure portal, select **Notebook VMs** on the left.

1. Select **+New** to create a notebook VM.

     ![Select New VM](./media/quickstart-run-cloud-notebook/add-workstation.png)

1. Provide a name for your VM. Then select **Create**. 

    ![Create a new VM](media/quickstart-run-cloud-notebook/create-new-workstation.png)

1. Wait approximately 4-5 minutes, then select **Refresh**.  Try refreshing every 30 seconds or so until the status is **Running**.

    ![Refresh](media/quickstart-run-cloud-notebook/refresh.png)

## Launch Jupyter web interface

After your VM is running, use the **Notebook VMs** section to launch the Jupyter web interface.

1. Select **Jupyter** in the **URI** column for your VM.  

    ![Start the Jupyter notebook server](./media/quickstart-run-cloud-notebook/start-server.png)

    The link starts your notebook server and opens the Jupyter notebook webpage in a new browser tab.  This link will only work for the person who creates the VM.

1. On the Jupyter notebook webpage, select the **samples/quickstart** folder to see the quickstart notebook.

## Run the notebook

Run a notebook that estimates pi and logs the error to your workspace.

1. Select **01.run-experiment.ipynb** to open the notebook.

1. You may see a message that the kernel has not been set.  Select **Python 3.6 - AzureML**, then select **Set Kernel**.

   ![Set the kernel](./media/quickstart-run-cloud-notebook/set-kernel.png)

1. The status area tells you to wait until the kernel has started. The message disappears once the kernel is ready.

    ![Wait for kernel to start](./media/quickstart-run-cloud-notebook/wait-for-kernel.png)

1.  Click into the first code cell and select **Run**.

    > [!NOTE]
    > Code cells have brackets before them. If the brackets are empty (__[  ]__), the code has not been run. While the code is running, you see an asterisk(__[*]__). After the code completes, a number **[1]** appears.  The number tells you the order in which the cells ran.
    >
    > Use **Shift-Enter** as a shortcut to run a cell.

    ![Run the first code cell](media/quickstart-run-cloud-notebook/cell1.png)

1. Run the second code cell. If you see instructions to authenticate, copy the code and follow the link to sign in. Once you sign in, your browser will remember this setting.  

    > [!TIP]
    > Be sure not to copy the space after the code.  

    ![Authenticate](media/quickstart-run-cloud-notebook/authenticate.png)

1. When you are done, the cell number __[2]__ appears.  If you had to sign in, you will see a successful authentication status message.   If you didn't have to sign in, you won't see any output for this cell, only the number appears to show that the cell ran successfully.

    ![Success message](media/quickstart-run-cloud-notebook/success.png)

1. Run the rest of the code cells.  As each cell finishes running, you will see its cell number appear. Only the last cell displays any other output.  In the largest code cell, you see `run.log`  used in multiple places. Each `run.log` adds its value to your workspace.


## View logged values

1. The output from the `run` cell contains a link back to the Azure portal to view the experiment results in your workspace. 

    ![View experiments](./media/quickstart-run-cloud-notebook/view-exp.png)

1. Click the **Link to Azure portal** to view information about the run in your workspace.  This link opens your workspace in the Azure portal.

1. The plots of logged values you see were automatically created in the workspace. Whenever you log multiple values with the same name parameter, a plot is automatically generated for you.

   ![View history](./media/quickstart-run-cloud-notebook/web-results.png)

Because the code to approximate pi uses random values, your plots will show different values.  
