# Consuming your OData source with Excel 2016

Last year we added the feature to expose the data of your WEM application with OData. This allows other applications to easily access and modify the data of your application. In the article [Expose your data via OData](https://github.com/zoombim/Public-Documentation/tree/09466aea1b73d2e87a60fac4ae6557406b4c032f/public/documentation/tips-and-tricks.data.expose-data-odata) you can read how this works in WEM, and how you can load your data into Excel 2013.

In Microsoft Excel 2016, things have changed a little bit. To connect to an OData source, you still go to the **Data** tab, but then you choose **New Query** > **From Other Sources** > **From OData Feed**.

![Excel2016-OData-dropdown](https://github.com/zoombim/Public-Documentation/tree/09466aea1b73d2e87a60fac4ae6557406b4c032f/public-documentation/.gitbook/assets/tips-and-tricks.data.excel-2016-odata-dropdown.png)

You now get a popup where you can specify the URL to the OData feed. For this example, I again use the demo application [http://odata-demo.live.wem.io/odata/](http://odata-demo.live.wem.io/odata/). Make sure you add that last slash at the end of the url!

![Excel2016-OData-feed-popup](https://github.com/zoombim/Public-Documentation/tree/09466aea1b73d2e87a60fac4ae6557406b4c032f/public-documentation/.gitbook/assets/tips-and-tricks.data.excel-2016-odata-feed-popup.png)

After you click **Ok**, it will prompt you for the user credentials. Select **Basic** and enter the username and password. The username and password for the demo application are `demo` and `demo1234`.

![Excel2016-OData-credentials](https://github.com/zoombim/Public-Documentation/tree/09466aea1b73d2e87a60fac4ae6557406b4c032f/public-documentation/.gitbook/assets/tips-and-tricks.data.excel-2016-odata-credentials.png)

After you click on **Connect**, you will get a popup where you can choose which tables you want to import into Excel. In my case I choose "_Select multiple items_", and select all tables. Next, click on **Load**.

![Excel2016-OData-navigator](https://github.com/zoombim/Public-Documentation/tree/09466aea1b73d2e87a60fac4ae6557406b4c032f/public-documentation/.gitbook/assets/tips-and-tricks.data.excel-2016-odata-navigator.png)

The panel "Workbook Queries" will appear on the right side of excel. This panel will list all the tables you chose to import. When you hover over these tables, a popover will appear that will preview the data and allow you to edit the query. This allows you to apply filters, and to combine data from multiple tables. In my case I simply want to import all the data from the `Companies` table, so I click on the three dots (•••) and choose the option **Load To...**..

![Excel2016-OData-loadto](https://github.com/zoombim/Public-Documentation/tree/09466aea1b73d2e87a60fac4ae6557406b4c032f/public-documentation/.gitbook/assets/tips-and-tricks.data.excel-2016-odata-loadto.png)

I can now choose to view this data as a Table and either load it into a new worksheet, or into an existing worksheet. In my case, I choose _Existing worksheet_. Finally, I click on the button **Load**, and the data will be imported into Excel.

![Excl2016-OData-loadto-table](https://github.com/zoombim/Public-Documentation/tree/09466aea1b73d2e87a60fac4ae6557406b4c032f/public-documentation/.gitbook/assets/tips-and-tricks.data.excel-2016-odata-loadto-table.png)

Excel will store the connection to the OData feed in the excel document, so the next time you open this document, you can go back to the **Data** tab and click on the **Refresh** button to retrieve the updated data from the OData feed. If you want to see the workbook queries again, you can click on the button **Show Queries**.
