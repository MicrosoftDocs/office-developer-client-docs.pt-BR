---
title: Usar os utilitários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3f461d50e838aac0caee37d295ba8e86b9559bd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770699"
---
# <a name="using-the-mapi-utilities"></a><span data-ttu-id="8fe86-103">Usar os utilitários MAPI</span><span class="sxs-lookup"><span data-stu-id="8fe86-103">Using the MAPI Utilities</span></span>

  
  
<span data-ttu-id="8fe86-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8fe86-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8fe86-105">Os utilitários MAPI são compostos de dados da tabela e objetos de dados de propriedade e uma variedade de funções para dar suporte a diversos recursos.</span><span class="sxs-lookup"><span data-stu-id="8fe86-105">The MAPI utilities are made up of table data and property data objects and a variety of functions to support miscellaneous features.</span></span> <span data-ttu-id="8fe86-106">É possível para um cliente precisam apenas esses utilitários e não precisa fazer logon no subsistema de MAPI para estabelecer uma conexão com provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="8fe86-106">It is possible for a client to need only these utilities and not have to log on to the MAPI subsystem to establish a connection with service providers.</span></span> <span data-ttu-id="8fe86-107">Se seu cliente enquadra nessa categoria, chamar a função de API [ScInitMapiUtil](scinitmapiutil.md) , e não a função [MAPIInitialize](mapiinitialize.md) em tempo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="8fe86-107">If your client fits into this category, call the API function [ScInitMapiUtil](scinitmapiutil.md) rather than the [MAPIInitialize](mapiinitialize.md) function at initialization time.</span></span> 
  
 <span data-ttu-id="8fe86-108">**ScInitMapiUtil** permite aos clientes utilizarem funções do utilitário que exigem alocadores de MAPI, mas que não solicitará as alocadores explicitamente.</span><span class="sxs-lookup"><span data-stu-id="8fe86-108">**ScInitMapiUtil** enables clients to use utility functions that require MAPI allocators, but that do not ask for the allocators explicitly.</span></span> <span data-ttu-id="8fe86-109">Quando for tempo para serem desligados, chame [DeinitMapiUtil](deinitmapiutil.md) para liberar recursos ao invés [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="8fe86-109">When it is time to shut down, call [DeinitMapiUtil](deinitmapiutil.md) to free resources rather than [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="8fe86-110">Clientes que nunca chamada **MAPIInitialize** não devem chamar **MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="8fe86-110">Clients that never call **MAPIInitialize** should not call **MAPIUninitialize**.</span></span>
  
<span data-ttu-id="8fe86-111">Se você tiver telefonado **ScInitMapiUtil** em vez de **MAPIInitialize** e estiver usando tabelas por meio dos métodos **ITableData** , em vez de por meio dos métodos **IMAPITable** , lembre-se de que as notificações de tabela não funcionará.</span><span class="sxs-lookup"><span data-stu-id="8fe86-111">If you have called **ScInitMapiUtil** rather than **MAPIInitialize** and are using tables through the **ITableData** methods rather than through the **IMAPITable** methods, be aware that table notifications will not work.</span></span> <span data-ttu-id="8fe86-112">Notificações exigem o uso de bibliotecas de MAPI e [IMAPITable: IUnknown](imapitableiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="8fe86-112">Notifications require the use of the MAPI libraries and [IMAPITable : IUnknown](imapitableiunknown.md).</span></span>
  

