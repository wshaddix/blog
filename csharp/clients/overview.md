---
title: Clients
order: 60
---

# Clients

WinUI and Uno share this layer. Blazor borrows the HTTP and auth parts and keeps its own UI model.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## In this section

- [MVVM](/csharp/clients/mvvm) - CommunityToolkit.Mvvm, commands, and DI.
- [XAML](/csharp/clients/xaml) - Layout, binding, resources, and templates.
- [HTTP and auth](/csharp/clients/http-and-auth) - A typed client, a bearer handler, and Problem Details.
- [Navigation and storage](/csharp/clients/navigation-and-storage) - Navigation, settings, and secure token storage.
- [Accessibility](/csharp/clients/accessibility) - Keyboard, contrast, and automation properties.

## The rule

The client renders state and calls the API. It does not reimplement a rule the server enforces.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [WinUI 3](/csharp/winui/overview)
- [Uno Platform](/csharp/uno/overview)
- [Blazor](/csharp/aspnet-core/blazor/overview)

---

**Next:** [MVVM](/csharp/clients/mvvm)
