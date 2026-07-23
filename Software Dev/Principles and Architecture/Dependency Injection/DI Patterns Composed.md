
```C#
// Decorator
services.AddScoped<Service>();
services.AddScoped<IService>(provider =>
	new LoggedService(
		provider.GetRequiredService<Service>(),
		provider.GetRequiredService<ILogger>()
	));

// Composite
services.AddScoped<DesktopNotificationService>();
services.AddScoped<MobileNotificationService>();
services.AddScoped<INotificationService>(provider =>
    new CompositeNotificationService(
    [
        provider.GetRequiredService<DesktopNotificationService>(),
        provider.GetRequiredService<MobileNotificationService>()
    ]));
```