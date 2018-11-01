---
title: Provedores e componentes de serviços
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d215c7c66c489e54d513941604b1c66c0e9094c1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881206"
---
# <a name="service-providers-and-components"></a><span data-ttu-id="4ed0a-102">Provedores e componentes de serviços</span><span class="sxs-lookup"><span data-stu-id="4ed0a-102">Service Providers and Components</span></span>


<span data-ttu-id="4ed0a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ed0a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4ed0a-104">Provedores e componentes de serviços são componentes que estendem a funcionalidade de provedores de dados implementando interfaces estendidas que não são suportadas originariamente pelo repositório de dados.</span><span class="sxs-lookup"><span data-stu-id="4ed0a-104">Service providers are components that extend the functionality of data providers by implementing extended interfaces that are not natively supported by the data store.</span></span>

<span data-ttu-id="4ed0a-105">Microsoft Data Access fornece uma *arquitetura de componente* que permite que os componentes individuais, especializados implementar discretos define da funcionalidade de banco de dados ou "services", na parte superior de armazenamentos de menor capacidade.</span><span class="sxs-lookup"><span data-stu-id="4ed0a-105">Microsoft Data Access provides a *component architecture* that allows individual, specialized components to implement discrete sets of database functionality, or "services," on top of less capable stores.</span></span> <span data-ttu-id="4ed0a-106">Portanto, em vez de forçar cada repositório de dados a fornecer sua própria implementação de funcionalidade estendida ou de forçar aplicativos genéricos a implementar funcionalidades de bancos de dados internamente, os componentes de serviços fornecem uma implementação comum que qualquer aplicativo pode usar quando acessar qualquer repositório de dados.</span><span class="sxs-lookup"><span data-stu-id="4ed0a-106">Thus, rather than forcing each data store to provide its own implementation of extended functionality or forcing generic applications to implement database functionality internally, service components provide a common implementation that any application can use when accessing any data store.</span></span> <span data-ttu-id="4ed0a-107">O fato de algumas funcionalidades serem implementadas originariamente pelo repositório de dados e outras pelos componentes genéricos é transparente para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4ed0a-107">The fact that some functionality is implemented natively by the data store and some through generic components is transparent to the application.</span></span>

<span data-ttu-id="4ed0a-p102">Por exemplo, um mecanismo de cursor, como o Microsoft Cursor Service para OLE DB, é um componente de serviço que pode consumir dados de um repositório de dados sequencial e somente de encaminhamento para produzir dados roláveis. Outros provedores de serviços comumente usados pelo ADO incluem o Microsoft OLE DB Persistence Provider (para salvar dados em um arquivo), o Microsoft Data Shaping Service para OLE DB (para **Conjuntos de registros** hierárquicos) e o Microsoft OLE DB Remoting Provider (para chamar provedores de dados em um computador remoto)</span><span class="sxs-lookup"><span data-stu-id="4ed0a-p102">For example, a cursor engine, such as the Microsoft Cursor Service for OLE DB, is a service component that can consume data from a sequential, forward-only data store to produce scrollable data. Other service providers commonly used by ADO include the Microsoft OLE DB Persistence Provider (for saving data to a file), the Microsoft Data Shaping Service for OLE DB (for hierarchical **Recordsets**), and the Microsoft OLE DB Remoting Provider (for invoking data providers on a remote computer).</span></span>

<span data-ttu-id="4ed0a-110">Para obter mais informações sobre provedores de dados e serviços, consulte [Apêndice A: Provedores](appendix-a-providers.md).</span><span class="sxs-lookup"><span data-stu-id="4ed0a-110">For more information about service and data providers, see [Appendix A: Providers](appendix-a-providers.md).</span></span>

