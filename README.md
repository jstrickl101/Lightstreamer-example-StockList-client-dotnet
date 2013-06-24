
Lightstreamer StockList Demo Client for .NET
============================================

<table>
  <tr>
    <td style="text-align: left">
      &nbsp;<a href="http://www.lightstreamer.com/demo/DotNetDemo/DotNetClientDemo_N2.msi" target="_blank"><img src="http://www.lightstreamer.com/img/demo/screen_dotnet.png"></a>&nbsp;
      
    </td>
    <td>
      &nbsp;Click here to download and install the application:<br>
      &nbsp;<a href="http://www.lightstreamer.com/demo/DotNetDemo/DotNetClientDemo_N2.msi" target="_blank">http://www.lightstreamer.com/demo/Flash_StockListDemo_Basic/</a>
    </td>
  </tr>
</table>

This is a .NET version of the [Stock-List Demos](https://github.com/Weswit/Lightstreamer-example-Stocklist-client-javascript), where thirty items are subscribed to.<br>

This app uses the <b>.NET Client API for Lightstreamer</b> to handle the communications with Lightstreamer Server. A simple user interface is implemented to display the real-time data received from Lightstreamer Server.
The application uses a grid to display the real-time data. You can resize and drag the columns around.


Build and Run the Demo
----------------------

The example is comprised of the following source code and image files:
* Source/*
* Properties/*
* Images/*

Once you have generated the Demo Client binaries (DotNetClientDemo_N2.exe) you should create a deploy folder, let's call it "Deployment", and copy the binaries here. Then get the .NET Client API for Lightstreamer binaries files (DotNetClient_N2.dll, DotNetClient_N2.pdb) from the [Lightstreamer 5 Colosseo distribution](http://www.lightstreamer.com/download) and put them in the "Deployment" folder.
Now you can prepare a  DotNetClient.bat launch script such this:
```cmd
@echo off

rem ---------------------------------------------------------------------------
rem Set the DotNet installation path as the current directory. Change the 
rem directory accordingly to your installation path of DotNet Adapter.

pushd .


rem ---------------------------------------------------------------------------
rem Start the StockList Demo Client, specifiyng to connect to the local
rem Lightstreamer Server instance.

start "DotNetStockListDemo" DotNetStockListDemo localhost 8080


rem ---------------------------------------------------------------------------
rem All done. Goes back to the original current directory and pauses, in case 
rem of any error.

echo Processes started. All done.
popd
pause
```

The DotNetClientDemo_N2 executable can also be run by double-clicking it; in its default configuration, the client will try to connect to Lightstreamer server at http://localhost:80.
In this case the [QUOTE_ADAPTER](https://github.com/Weswit/Lightstreamer-example-Stocklist-adapter-java) and [LiteralBasedProvider](https://github.com/Weswit/Lightstreamer-example-ReusableMetadata-adapter-java) have to be deployed in your local Lightstreamer server instance. The factory configuration of Lightstreamer server already provides this adapter deployed.<br>


See Also
--------

* [Lightstreamer StockList Demo Client for JavaScript](https://github.com/Weswit/Lightstreamer-example-Stocklist-client-javascript)
* [Lightstreamer StockList Demo Adapter](https://github.com/Weswit/Lightstreamer-example-Stocklist-adapter-java)
* [Lightstreamer Reusable Metadata Adapter in Java](https://github.com/Weswit/Lightstreamer-example-ReusableMetadata-adapter-java)

Lightstreamer Compatibility Notes
---------------------------------

- Compatible with Lightstreamer .NET Client Library version 2.1.4588.28986 or newer.