# M13-Interview-Task-02
Back-end task test, Client application development

### Code Updates.

1.	Added try catch blogs to capture process errors
```csharp
try
{
    lock (Rules)
    {
        if (Rules.ContainsKey(site))
        {
            Rules.Remove(site);
        }

        Rules.Add(site, rule);
    }
}
catch (Exception ex)
{
    TempData["ErrorMessage"] = "There was an error processing your request.";
    _logger.LogInformation("Add Site Error. " + ex.ToString());
}
```
2.	Added NLog to log errors that occur
```csharp
_logger.LogInformation("Add Site Error. " + ex.ToString());
```
3.	Formatted data received in readable html data
![HomeApi](https://i.ibb.co/k95fBM0/ApiHome.jpg)
4.	Added error messages in view for process failures
![ErrorRequest](https://i.ibb.co/ypdhFzn/Error-Request.jpg)

### Total time took approximately 1:15 mins
