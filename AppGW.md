# Building an Application Gateway
[Back to Main](README.md)

From the Azure Portal, search for "Application Gateway" and click to create a new one.

Before building one, be sure you have a proper /27 subnet created specifically for this.

![image](https://user-images.githubusercontent.com/16612216/148796012-c695ee34-2a6f-4164-8bfc-c97ea4e8d113.png)

You'll want to create a new public IP for this gateway.

![image](https://user-images.githubusercontent.com/16612216/148796135-a1d462b8-84ad-42bc-8c63-81e9718f6b20.png)

For the backend pool, create one that targets the FQDN for your APIM instance:

![image](https://user-images.githubusercontent.com/16612216/148796365-f632d432-ee54-4a5b-94f9-673c29b8a47a.png)

For building out the routing rule, there are a few steps.  This ties requests from the front-end, to services on the back end.

We start with the routing rule and it's listener config.

![image](https://user-images.githubusercontent.com/16612216/148796746-5dcfdade-45fa-4e51-8f61-e62f01643ba1.png)

The Backend targets will link the listener to something:

![image](https://user-images.githubusercontent.com/16612216/148796837-d49a0410-db3b-4281-a2d2-b3f1ef065977.png)

There's an HTTP setting component as well:

![image](https://user-images.githubusercontent.com/16612216/148796716-b82716d3-30f9-49de-a22a-b8bcde74011b.png)
