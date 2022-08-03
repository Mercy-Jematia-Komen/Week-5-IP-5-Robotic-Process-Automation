rename the Request file as Request + Date Timestamp before moving it to the Requests folders. using below steps:

Consider your file path is stored in the below string variable.
strFilePath = "C:\Users\Mkomen\Zoho\Requests Request.xlsx"

Assign Activity for setting new file path with a date (create one string variable).
strnewFilePath = strFilePath.Substring(0, strFilePath.Length - 5) + "_" + DateTime.Now.ToString(“yyyyMMdd”) + “.xlsx”

After assign activity, strnewFilePath contains the following value -

C:\Users\Mkomen\Zoho\Requests  Request_20220803.xlsx

In the properties of Move File Activity, set the following
Path - strFilePath
Destination - strnewFilePath
