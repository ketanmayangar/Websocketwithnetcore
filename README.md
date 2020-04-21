# Websocketwithnetcore
Websocket with .net core example
.Net core using web socket example
local address kept as 0.0.0.0:9000
as this address websocket will also connect.

There is a middleware for socket invoke and recive message

the middleware is used in the application in the config method
public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
{
.....
app.MapWebSocketManager("/ws", serviceProvider.GetService<WebsocketExampleMessageHandler>());
....
}


and in Program.cs define
webBuilder.UseUrls("http://0.0.0.0:9000");
