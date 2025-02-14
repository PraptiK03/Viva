---
title: "About Viva Engage networks and Microsoft 365 tenants"
f1.keywords:
- NOCSH
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
ms.date: 01/23/2025
audience: Admin
ms.topic: overview
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Viva Engage
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 85516b0c-79ad-4483-8534-4477c8d26e1a
description: "Understand the relationship between a Viva Engage network and a Microsoft 365 tenant."
---

# Viva Engage networks and Microsoft 365 tenants

To provide the best end-user and management experience, every Microsoft 365 tenant is associated with a single Viva Engage network. If you don't have this configuration, we strongly recommend that you [consolidate previously migrated networks](consolidate-multiple-networks.md) into a single primary network for your tenant. By doing so, you move Viva Engage into a supported state for your tenant, and protect your networks from automatic consolidation.
 
> [!NOTE]
> When you receive a communication from Viva Engage stating that your Microsoft 365 tenant is associated with two or more Viva Engage networks, read this article for more context. Also see the more detailed [blog post from Viva Engage support](https://askyammer.github.io/post/2016-04-15-your-office365-tenant-is-associated-with-two-or-more-canonical-home-yammer-networks/) for information about what actions you can take. 
 
## The changing role of the Viva Engage network

A Viva Engage network represents people who are part of the same organization, and work together closely. A Viva Engage network acts as an organizational boundary and as a management entity. As Viva Engage becomes an integral part of Microsoft 365, Viva Engage uses the associated Microsoft 365 tenant as the organizational boundary and for managing key functions.
 
**Viva Engage network as an organizational boundary**: Only users who are part of the same organization can join the network, which provides trust between members of the network, so they can collaborate freely.
 
All Microsoft 365 apps, including Viva engage, share the same organizational boundary. All Microsoft 365 users who are part of the same Microsoft 365 tenant (with a Viva Engage subscription) can access Viva Engage.
 
When you add a new domain to the Microsoft 365 tenant, that domain automatically synchronizes with Viva Engages, so users of the new domain can access it.
 
**Viva Engage network as a management entity**: The Viva Engage service is managed in Microsoft 365 as a standard service. It supports the same identity, domain, user, and license management features as all other Microsoft 365 apps. You use one set of tools for Microsoft 365 administrators to manage all Microsoft 365 services, including for Viva Engage. 

We recommend that Viva Engage Administrators only manage Viva Engage-specific configurations (such as notification defaults or External network settings) at the network level.
 
## Associate Viva Engage networks with Microsoft 365 tenants

Several customers adopted Viva Engage before it was closely integrated with Microsoft 365, which resulted in the following configurations.
 
### One Microsoft 365 tenant associated with one Viva Engage network

In this scenario, your Microsoft 365 tenant is associated with a single Viva Engage network. For example:
 
- **Verified domains on the Microsoft 365 tenant:** `contoso.onmicrosoft.com`, `contoso.com`, `fabrikam.com`

- **Domains on Viva Engage network:** `contoso.onmicrosoft.com`, `contoso.com`, `fabrikam.com`
 
**How customers get into this configuration:** Viva Engage is on by default in Microsoft 365. When you create a new Microsoft 365 tenant, it also creates a new Viva Engage network. Viva Engage adds the domains from Microsoft 365. Viva Engage also activates for all tenants with a Microsoft 365 Viva Engage premium subscription. Whenever domains are added to or removed from the Microsoft 365 tenant, the domains always synchronize with the Viva Engage network.
 
This configuration is standard. Key benefits of this configuration include:
 
- **Reduce Viva Engage administration cost:** You can manage one single Viva Engage service, rather than managing individual Viva Engage networks.

- Manage the Viva Engage service seamlessly from Microsoft 365, using the same method for other Microsoft 365 services. You can manage the lifecycle of all Viva Engage users centrally in Microsoft 365, and you can manage the lifecycle of Viva Engage domains from Microsoft 365.

- **Reduce information silos in your organization:** All your users share a consolidated Viva Engage service, which empowers them to connect and work with anyone in your organization.

This configuration supports the following capabilities related to managing Viva Engage in Microsoft 365.
 
|Capability|Support in the one tenant/one network configuration|
|:-----|:-----|
|Sign-in <br/> |Yes <br/> |
|Single sign-on <br/> |Yes <br/> |
|User lifecycle management <br/> |Yes <br/> |
|Administrator lifecycle management <br/> |Yes <br/> |
|License management <br/> |Yes <br/> |
|Domain lifecycle management <br/> |Yes <br/> |
|Future Viva Engage-Microsoft 365 Groups Integration <br/> |Yes <br/> |
|Other future Viva Engage-Microsoft 365 integrations <br/> |Yes <br/> |

**Viva Engage-Microsoft 365 groups integration:** Microsoft 365 connected groups are only available to customers in the one tenant/one network configuration.
 
For information about managing your tenant in this configuration, see [Manage Viva Engage domains across their lifecycle](manage-viva-engage-domains.md).
 
### One Microsoft 365 tenant, many networks

<a name="OneTenantManyNetworks"> </a>

In this scenario, your Microsoft 365 tenant associates with two or more Viva Engage networks. For example:
 
- **Verified domains on the Microsoft 365 tenant:** `contoso.onmicrosoft.com`, `contoso.com`, `fabrikam.com`

- **Domains on Viva Engage network #1:** `contoso.onmicrosoft.com`, `contoso.com`

- **Domains on Viva Engage network #2:** `fabrikam.com`
 
**How customers get into this configuration**: This scenario is common with large customers. 

A large organization (`contoso.com`) has several subsidiaries (suppose `fabrikam.com` is one of them). The organization itself has an official Microsoft 365 tenant and an official Viva Engage network (`contoso.com` network). Users in subsidiary companies might independently sign up for their own Viva Engage networks with separate own email domains (`fabrikam.com network`). 

Large companies can use dozens of Viva Engage networks. Many subsidiary networks are lightly used or unused, most likely because they're separate from the more active larger network. 

The organization must consolidate these smaller networks into the larger parent network by performing [network migration](consolidate-multiple-networks.md). After consolidation, the organization realizes a key benefit of single-tenant operation: one network configuration.
 
Even after consolidation, you might be in a situation where due to strong business reasons, one Microsoft 365 tenant connects with several Viva Engage networks. **This is not a supported configuration. Until you consolidate, you will experience the following limitations:**
 
- **Increased Viva Engage administration cost:** You have to manage multiple Viva Engage networks, which increases administration costs.

- **Inability to collaborate with everyone in the organization:** All employees of your organization aren't on the same Viva Engage network, so users aren't able to connect with everyone in the organization using Viva Engage. For example:

- **Company-wide announcements**: If the CEO of the company needs to communicate a message to everyone in the organization, they must do it in every network individually. Employee reactions to the announcement aren't available to everyone in the organization.

- **Organic information discovery**: If employees in one network are working on a project and need to refer to a similar project in another subsidiary, they can't access it. Lack of access directly impacts organic collaboration.

- **Confusion caused due to organization boundaries being different in Viva Engage vs. Microsoft 365:** In this configuration, the organizational boundary in Microsoft 365 is larger than the individual Viva Engage networks, causing potential confusion. 

For example, a Microsoft 365 video is shared with everyone in the organization. A `contoso.com` network user comments on the video, but other users in the `contoso.com` network are the only ones who can see it. A `fabrikam.com` network user adds another comment to the same video, but this comment isn't visible to the `contoso.com` user, because they're on different networks.

- **Viva Engage-Microsoft 365 groups integration not available:** As announced in the Viva Engage blog, we're working on integrating Viva Engage groups with Microsoft 365 groups infrastructure. This feature isn't available to customers in the one tenant: many network configurations. Organizational boundaries between Microsoft 365 and Viva Engage can also cause this problem. Here's an example.

- **Group membership management**: A company integrates the Viva Engage groups with the Microsoft 365 groups infrastructure. A group is created in the `contoso.com` network that contains only users who can be part of the `contoso.com` network. When this integrated group is managed in Microsoft 365, a user with the `fabrikam.com` domain can be added to the group. Now this `fabrikam.com` user can't be added to the group in Viva Engage.

Here's a list of key capabilities (related to managing Viva Engage in Microsoft 365) that you can use in this configuration.
 
|Capability|In the one tenant/many networks configuration|
|:-----|:-----|
|Sign-in <br/> |Yes <br/> |
|Single sign-on <br/> |Yes <br/> |
|User lifecycle management <br/> |Yes <br/> |
|Administrator lifecycle management <br/> |Yes <br/> |
|License management <br/> |Yes <br/> |
|Domain lifecycle management <br/> |Yes <br/> |
|Future Viva Engage-Microsoft 365 Groups Integration <br/> |No <br/> |
|Other future Viva Engage-Microsoft 365 integrations <br/> |No <br/> |

 **Sign-in:** Even when a Microsoft 365 tenant is associated with many Viva Engage networks, one Microsoft 365 user is associated with just one Viva Engage network. And when users access Viva Engage, they land in the correct network.
 
- Linda and John are users of the same Microsoft 365 tenant, but they're members of different networks. If `linda@contoso.com` tries to access Viva Engage by selecting the Viva Engage tile or by logging in at `www.Viva Engage.com`, the system prompts Linda for their Microsoft 365 credentials, and joins the `contoso.com` network. 

Similarly, `john@fabrikam.com` can access Viva Engage, sign in with Microsoft 365 credentials, and join the `fabrikam.com network`. If Linda or John is a previous Viva Engage user, their Microsoft 365 account associates with their already existing Viva Engage user. No new user is created.

- Lorena is a Microsoft 365 tenant user, with multiple emails that correspond to multiple networks. Suppose that Lorena tries to access Viva Engage using `Lorena@contoso.com`. Lorena's primary email is `Lorena@contoso.com`, but they also have a proxy email `Lorena@fabrikam.com`. In this scenario, Lorena is prompted for their Microsoft 365 credentials, and lands on the `contoso.com` network. (Lorena is associated with just one of the Viva Engage networks.)

    - If the user's primary email matches a network, the user signs in to that network.

    - Else, if the user's nonprimary email matches the network, the user is logged into that network. If there are more than one nonprimary email matches, one of them is chosen.

    - Else, if the user's UPN (User Principal Name, such as `user@domain.com`) matches the network, the user is logged in to that network.

    - If this user was a Viva Engage user before, the Microsoft 365 account is associated with that already existing Viva Engage user (no new user is created).

  To access the other network, Lorena can do the following tasks.

    - Get invited as a guest from the other fabrikam.com network. If both networks are configured to use the **Enforce Microsoft 365 identity** configuration, this option is the only option.

    - Create a new account in the other network, and sign in with email and password.

After all users in the tenant can sign in to the network with their Microsoft 365 accounts, you can manage the lifecycle of all users in Microsoft 365 and also set up Microsoft 365 single sign-on.

 **Administrator lifecycle management:** Administrators in the Microsoft 365 Global administrator role for the Microsoft 365 tenant add the [Viva Engage Verified Administrators](../eac-key-admin-roles-permissions.md#verified-administrator) role for the matching networks. 
 
 After the admin's user account loses the Microsoft 365 Global administrator role, they also lose the Verified Administrators role on Viva Engage. 
 
 In the previous example, if a global admin has two emails, `admin@contoso.com` and `admin@fabrikam.com`, they become a Verified Administrator to the `contoso.com` network and to the `fabrikam.com` network. They can only sign in to one network with their Microsoft 365 credentials.

 **Domain lifecycle management:** When a Microsoft 365 tenant is associated with several Viva Engage networks, you can still manage Viva Engage domains across their lifecycle in Microsoft 365.

- When you add a domain in Microsoft 365, it's automatically added to the primary network designated for domain lifecycle management. When Viva Engage is activated in the Microsoft 365 tenant, the network with the largest number of activated users is designated as the primary network. Any new domains are added to the largest network. The `.onmicrosoft.com` domain on the Microsoft 365 tenant (the domain that can't be removed from the tenant) is also added to this primary network.

- When a domain is removed in Microsoft 365, it's removed from the corresponding network. If the domain is the last domain on the network, the network is disabled.

You have the following options to move to a one tenant/one network configuration:

- Consolidate the smaller networks into the larger network by performing [network migration](consolidate-multiple-networks.md). In the previous example, do the following:

 1. Ensure that Viva Engage is activated on your Microsoft 365 tenant. 

 2. If necessary, perform [Viva Engage Enterprise activation](../get-started-with-viva-engage/admin-quick-start.md) and activate Viva Engage on the domain associated with the larger parent network (in this case, `contoso.com`).

3. Navigate to the **Network migration** section (part of the Viva Engage administration pages) and migrate the smaller fabrikam.com network into the `contoso.com` network.  
   To do this operation, you need to be a Viva Engage verified administrator and a Global Administrator. At the end, you reach the following state:

   | Domains on the Microsoft 365 tenant | Domains on the Viva Engage network |
   |:------------------------------------|:------------------------------------|
   | `Contoso.onmicrosoft.com`<br/> `Contoso.com`<br/> `Fabrikam.com`<br/> | `Contoso.onmicrosoft.com`<br/> `Contoso.com`<br/> `Fabrikam.com`<br/> |

- If the subsidiary is fully assimilated with the parent organization, or is spun off, you can remove the subsidiary company's domain from the Microsoft 365 tenant. In the previous example, you remove fabrikam.com from the Microsoft 365 tenant. At the end, you reach the following state:

  |Domains on the Microsoft 365 tenant|Domains on the Viva Engage network|
  |:-----|:-----|
  |`Contoso.onmicrosoft.com`<br/> `Contoso.com`<br/> |`Contoso.onmicrosoft.com`<br/> `Contoso.com`<br/> |

### Many Microsoft 365 tenants associated with one Viva Engage network (many tenants/one network)

Two or more Microsoft 365 tenants might belong to a single Viva Engage network. For example:

- **Verified domains on the Microsoft 365 tenant1:** `contoso.onmicrosoft.com`, `contoso.com`

- **Verified domains on the Microsoft 365 tenant2:** `fabrikam.onmicrosoft.com`, `fabrikam.com`

- **Domains on Viva Engage network:** `contoso.com`, `fabrikam.com`

**How customers get into this configuration:** Typically, large customers find themselves in this scenario. A large organization (`contoso.com`) could have several subsidiaries (say fabrikam.com is one of them). This organization has a Viva Engage network and can add all the domains in the company to the Viva Engage network. While the organization itself has an official Microsoft 365 tenant, the subsidiary company might independently create another Microsoft 365 tenant (fabrikam.com).

 **This is not a supported configuration.** Only one tenant associates with Microsoft 365 for management and sign in processes. The following table shows the key capabilities for managing Viva Engage in Microsoft 365 that are supported (or not) in this configuration.

|Capability|Support in many tenants: one network configuration|Details|
|:-----|:-----|:-----|
|Sign-in<br/> |No <br/> |Users from only one of the Microsoft 365 tenants can sign in to Viva Engage with their Microsoft 365 sign-in. The first user that signs in using Microsoft 365 credentials determines which Microsoft 365 tenant gets associated with the Viva Engage network for sign-in. <br/> |
|Single sign-on <br/> |No <br/> |Since not all users can sign in to Viva Engage with their Microsoft 365 credentials, you can't [Enforce Microsoft 365 identity](enforce-office-365-identity.md) in Viva Engage, and implement the Microsoft 365 based single sign-on solution. The Microsoft 365 based single sign-on solution can't be implemented in the many tenants: one network configuration. <br/> |
|User lifecycle management <br/> |No <br/> |User lifecycle can be managed only for users who can sign in to Viva Engage with their Microsoft 365 credentials. So, you can't manage all Viva Engage users across their life cycle in Microsoft 365. <br/> |
|Administrator lifecycle management <br/> |No <br/> |Only Global administrators of one of the tenants is added as Verified Administrators in Viva Engage. So, you can't manage the lifecycle of all Viva Engage administrators across their life cycle in Microsoft 365. <br/> |
|License management <br/> |No <br/> |Licenses can be managed only for users who can sign in to Viva Engage with their Microsoft 365 credentials. Also, since you can't [Enforce Microsoft 365 identity](enforce-office-365-identity.md), you can't block Microsoft 365 users without Viva Engage licenses. <br/> |
|Domain lifecycle management <br/> |No <br/> |This configuration isn't supported for domain lifecycle management, so you can't [Manage Viva Engage domains across their lifecycle in Microsoft 365](manage-viva-engage-domains.md). <br/> |
|Consolidating free Viva Engage basic networks <br/> |Yes <br/> |You can sign in to Viva Engage, and consolidate Viva Engage basic network to the Microsoft 365 tenant directly associated with the Viva Engage network for management. <br/> |
|Future Viva Engage-Microsoft 365 Groups Integration <br/> |No <br/> ||
|Other future Viva Engage-Microsoft 365 integrations <br/> |No <br/> ||

You have the following options to move out of this unsupported configuration:

- Add all the relevant domains to one tenant using the Microsoft 365 admin center.  
  In the previous example, you ensure that both `contoso.com` and `fabrikam.com` are on the same tenant.  
  At the end, you reach the following state:

  | Domains on the Microsoft 365 tenant | Domains on the Viva Engage network |
  |:-----------------------------------|:----------------------------------|
  | `Contoso.onmicrosoft.com` <br/> `Contoso.com` <br/> `Fabrikam.com` | `Contoso.onmicrosoft.com` <br/> `Contoso.com` <br/> `Fabrikam.com` |

- Create separate Viva Engage networks, one per tenant. In the previous example, you remove either `contoso.com` or `fabrikam.com` from the Viva Engage network, and create a new network with that domain. To remove Viva Engage domains from your network, contact the [Viva Engage Support](https://support.microsoft.com/contactus) team. Before removing a domain from a network, delete all the user accounts containing that domain. If needed, these users can later be invited as guests from the newly created network. At the end, you reach the following state:

  | Domains on the Microsoft 365 tenant1 | Domains on the Viva Engage network |
  |:------------------------------------|:----------------------------------|
  | `Contoso.onmicrosoft.com` <br/> `Contoso.com` | `Contoso.onmicrosoft.com` <br/> `Contoso.com` |

  | Domains on the Microsoft 365 tenant2 | Domains on the Viva Engage network |
  |:------------------------------------|:----------------------------------|
  | `Fabrikam.onmicrosoft.com` <br/> `Fabrikam.com` | `Fabrikam.onmicrosoft.com` <br/> `Fabrikam.com` |

After you move into a one tenant/one network configuration, you might accidentally move back to a many tenants: one network configuration. Say, due to some reason the `contoso.com` network has another domain `tailspin.com`, which isn't added to the Microsoft 365 tenant. In this situation, a new Microsoft 365 tenant is created for `tailspin.com`. Now two tenants (`contoso.com` and `tailspin.com`) are connected to the same Viva Engage network. **To avoid this situation, we recommend that you add all the domains in your Viva Engage network to your Microsoft 365 tenant.** If you find yourself in this situation, use the previous guidance to get back to the recommended one tenant/one network configuration.

### FAQ

 **Q: One of our users is redirected to the wrong Viva Engage network.**

A: This issue happens if your network's in an unsupported configuration with one tenant and multiple Viva Engage networks. For more information, see the [One tenant: many Viva Engage networks scenario](#OneTenantManyNetworks) section.

You can [consolidate your Viva Engage networks](consolidate-multiple-networks.md), or change the user's account. For more information, see [A Viva Engage user is displayed as former member when you use Microsoft 365 sign-in for Viva Engage](../troubleshoot-problems/viva-engage-user-is-displayed-as-former-member.md).
