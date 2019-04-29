---
title: Usando os utilitários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d8ec18ee7b80d8603266cf827f9484ee85bdb03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409983"
---
# <a name="using-the-mapi-utilities"></a><span data-ttu-id="0dc8b-103">Usando os utilitários MAPI</span><span class="sxs-lookup"><span data-stu-id="0dc8b-103">Using the MAPI Utilities</span></span>

  
  
<span data-ttu-id="0dc8b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dc8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dc8b-105">Os utilitários MAPI são compostos de dados de tabela e objetos de dados de propriedade e uma variedade de funções para dar suporte a recursos diversos.</span><span class="sxs-lookup"><span data-stu-id="0dc8b-105">The MAPI utilities are made up of table data and property data objects and a variety of functions to support miscellaneous features.</span></span> <span data-ttu-id="0dc8b-106">É possível que um cliente precise apenas desses utilitários e não precise fazer logon no subsistema MAPI para estabelecer uma conexão com os provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="0dc8b-106">It is possible for a client to need only these utilities and not have to log on to the MAPI subsystem to establish a connection with service providers.</span></span> <span data-ttu-id="0dc8b-107">Se o cliente couber nessa categoria, chame a função da API [ScInitMapiUtil](scinitmapiutil.md) em vez da função [MAPIInitialize](mapiinitialize.md) no momento da inicialização.</span><span class="sxs-lookup"><span data-stu-id="0dc8b-107">If your client fits into this category, call the API function [ScInitMapiUtil](scinitmapiutil.md) rather than the [MAPIInitialize](mapiinitialize.md) function at initialization time.</span></span> 
  
 <span data-ttu-id="0dc8b-108">O **ScInitMapiUtil** permite que os clientes usem funções utilitárias que exigem alocadores MAPI, mas que não solicitam os alocadores explicitamente.</span><span class="sxs-lookup"><span data-stu-id="0dc8b-108">**ScInitMapiUtil** enables clients to use utility functions that require MAPI allocators, but that do not ask for the allocators explicitly.</span></span> <span data-ttu-id="0dc8b-109">Quando for o momento de desligar, chame [DeinitMapiUtil](deinitmapiutil.md) para liberar recursos, em vez de [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="0dc8b-109">When it is time to shut down, call [DeinitMapiUtil](deinitmapiutil.md) to free resources rather than [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="0dc8b-110">Clientes que nunca chamam **MAPIInitialize** não devem chamar **MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="0dc8b-110">Clients that never call **MAPIInitialize** should not call **MAPIUninitialize**.</span></span>
  
<span data-ttu-id="0dc8b-111">Se você chamou **ScInitMapiUtil** em vez de **MAPIInitialize** e está usando tabelas por meio dos métodos **ITableData** , e não através dos métodos IMAPITable, lembre-se de que as notificações de tabela não funcionarão. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="0dc8b-111">If you have called **ScInitMapiUtil** rather than **MAPIInitialize** and are using tables through the **ITableData** methods rather than through the **IMAPITable** methods, be aware that table notifications will not work.</span></span> <span data-ttu-id="0dc8b-112">As notificações exigem o uso das bibliotecas MAPI e [IMAPITable: IUnknown](imapitableiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="0dc8b-112">Notifications require the use of the MAPI libraries and [IMAPITable : IUnknown](imapitableiunknown.md).</span></span>
  

