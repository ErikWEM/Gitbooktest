# Expose your data via OData

## Expose your data via OData

WEM supports for OData. OData is an open protocol that allows you to consume or expose data through simple web requests. It builds upon the ideas of REST. Introduced by Microsoft in 2007, it is adopted by OASIS as a standard and supported by [a large number of applications](http://www.odata.org/ecosystem/).

OData is comparable with ODBC and JDBC, as it allows you to communicate with an (often relational) database in a similar manner. It allows you to query, insert, edit or delete data, all through simple HTTP requests. An OData service shares the schema of the exposed data, which makes it possible for the client application to discover all the table and column definitions.

With WEM, you can both consume external OData sources and expose the database of your application as an OData service. In this blog post I will show you how to do the latter.

### Example application

For this article we created a simple WEM application that stores product information about laptops, tablets and smartphones. This application is accessible via [https://odata-demo.live.wem.io](https://odata-demo.live.wem.io).

### Enabling OData

Enabling OData for your WEM application is as simple as creating an OData account. You can do this on the project settings page. When you select a portal (in many cases, the portal is just called "Default"), you will see the button **Manage OData users** appear in the toolbar.

Here you can create a new OData user. Make sure that the password is secure, for these login credentials allows anyone full access to all the data of your WEM application.

![](https://github.com/zoombim/Public-Documentation/tree/09466aea1b73d2e87a60fac4ae6557406b4c032f/public-documentation/.gitbook/assets/tips-and-tricks.data.create-odata-user.png)

Don't forget to save the project settings after you created the OData user. If you want to test the OData connection to your application via the staging or live URLs, then you have to publish your application as well.

#### Test the OData service in the browser

After you have created the OData user, saved your project settings and published your application, you can test the OData service in the browser. Type in the URL of your application followed by **/odata**. The browser will prompt you for the user credentials. The OData URL for the demo application is:

[**https://odata-demo.live.wem.io/odata**](https://odata-demo.live.wem.io/odata)\
(the username and password for the demo website are `demo` and `demo1234`)

You should see an XML document that describes which collections (persistent lists) are available in your WEM application. You can also view the detailed schema information by appending **/$metadata** to the url:

[**https://odata-demo.live.wem.io/odata/$metadata**](https://odata-demo.live.wem.io/odata/$metadata)\
(the username and password for the demo website are `demo` and `demo1234`)

If you want to learn more about using OData directly from your browser, you can read the [official documentation](http://www.odata.org/documentation/odata-version-3-0/odata-version-3-0-core-protocol/).

### Connect to your application via Excel

**remark**": if you want to use Excel 2016, please read the [article that deals with Excel 2016](https://github.com/zoombim/Public-Documentation/tree/09466aea1b73d2e87a60fac4ae6557406b4c032f/public/documentation/tips-and-tricks.data.odata-excel2016) specifically! The steps below don't work for Excel 2016.

Excel can connect to any OData source. This allows you to directly view the data, create pivot tables, generate charts, etc. Excel can not alter the exposed data, Microsoft never implemented that feature.

To connect to an OData source from Excel, go to the **DATA** tab, and choose **From Other Sources** and then **From OData Data Feed**. This will start the data connection wizzard. The first step asks for the URL and user credentials of the OData connection.

![](https://github.com/zoombim/Public-Documentation/tree/09466aea1b73d2e87a60fac4ae6557406b4c032f/public-documentation/.gitbook/assets/tips-and-tricks.data.excel-connect-to-odata.png)\
(the password for the odata demo application is `demo1234`)

The second step allows you to select which tables you want to connect to. For this example, I just select the **Products** table.

![](https://github.com/zoombim/Public-Documentation/tree/09466aea1b73d2e87a60fac4ae6557406b4c032f/public-documentation/.gitbook/assets/tips-and-tricks.data.excel-select-tables.png)

Excel stores the odata connection settings in an external `.odc` file. Afterwards you can reuse this connection via the toolbar icon **Existing Connections**. In the next step you can change the name and location of this file. You can also choose to store the login credentials in the file. For this example, I leave everything unchanged and click on **Finish**.

![](https://github.com/zoombim/Public-Documentation/tree/09466aea1b73d2e87a60fac4ae6557406b4c032f/public-documentation/.gitbook/assets/tips-and-tricks.data.excel-odc-file.png)

The final step allows you to configure how you want to show the data in Excel. For this example, I just choose **Table**. This will show all the rows that are stored in database of your WEM application.

![](https://github.com/zoombim/Public-Documentation/tree/09466aea1b73d2e87a60fac4ae6557406b4c032f/public-documentation/.gitbook/assets/tips-and-tricks.data.excel-import-data.png)

When this is done, you should see your data in Excel. You can now sort and filter the data using the standard Excel features. Note that Excel won't automatically synchronize the data. To see all the updates since the last time the data was imported, you can click on the button **Refresh All** (found in the **DATA** tab).
