---
title: Inicializando os utilitários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5c5a9355e9edec28e08986ccd055fc43eec7b974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420945"
---
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="66f1b-103">Inicializando os utilitários MAPI</span><span class="sxs-lookup"><span data-stu-id="66f1b-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="66f1b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66f1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66f1b-105">Se a única parte do MAPI que você precisa usar são os utilitários, as interfaces e funções declaradas no MAPIUTIL de MAPI. Arquivo de cabeçalho H como **IPropData** e **ITableData** — você não precisa chamar o **MAPIInitialize** para inicialização.</span><span class="sxs-lookup"><span data-stu-id="66f1b-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="66f1b-106">Para obter mais informações, consulte [IPropData: IMAPIProp](ipropdataimapiprop.md), [ITableData: IUnknown](itabledataiunknown.md)e [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="66f1b-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="66f1b-107">Em vez disso, chame a função **ScInitMapiUtil** .</span><span class="sxs-lookup"><span data-stu-id="66f1b-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="66f1b-108">Para obter mais informações, consulte [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="66f1b-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="66f1b-109">O **ScInitMapiUtil** permite que os aplicativos cliente usem funções e métodos de utilitários que exigem alocadores MAPI, mas que não pedem explicitamente.</span><span class="sxs-lookup"><span data-stu-id="66f1b-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="66f1b-110">No momento do desligamento, faça uma chamada para **DeinitMapiUtil** para liberar recursos conectados aos utilitários.</span><span class="sxs-lookup"><span data-stu-id="66f1b-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="66f1b-111">Não chame **MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="66f1b-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="66f1b-112">Para obter mais informações, consulte [DeinitMapiUtil](deinitmapiutil.md) e [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="66f1b-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="66f1b-113">Lembre-se de que a interface **ITableData** não oferece suporte a notificações de tabela para clientes que chamaram **ScInitMapiUtil** em vez de **MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="66f1b-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  

