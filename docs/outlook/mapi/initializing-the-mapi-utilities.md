---
title: Inicializar os utilitários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8ee0504d4a8b9e2ce96e42a53b778d4e3f518fcc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767556"
---
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="36796-103">Inicializar os utilitários MAPI</span><span class="sxs-lookup"><span data-stu-id="36796-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="36796-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="36796-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="36796-105">Se a única parte do MAPI que você precise usar são os utilitários — as funções e interfaces declaradas na MAPIUTIL do MAPI. Arquivo de cabeçalho H como **IPropData** e **ITableData** — não é necessário chamar **MAPIInitialize** para inicialização.</span><span class="sxs-lookup"><span data-stu-id="36796-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="36796-106">Para obter mais informações, consulte [IPropData: IMAPIProp](ipropdataimapiprop.md), [ITableData: IUnknown](itabledataiunknown.md)e [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="36796-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="36796-107">Em vez disso, chame a função de **ScInitMapiUtil** .</span><span class="sxs-lookup"><span data-stu-id="36796-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="36796-108">Para obter mais informações, consulte [ScInitMapiUtil](scinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="36796-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="36796-109">**ScInitMapiUtil** permite que os aplicativos cliente usar funções de utilitário e métodos que exigem alocadores de MAPI, mas que não pergunte explicitamente para eles.</span><span class="sxs-lookup"><span data-stu-id="36796-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="36796-110">No horário de desligamento, fazer uma chamada para **DeinitMapiUtil** para liberar recursos conectado aos utilitários.</span><span class="sxs-lookup"><span data-stu-id="36796-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="36796-111">Não chame **MAPIUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="36796-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="36796-112">Para obter mais informações, consulte [DeinitMapiUtil](deinitmapiutil.md) e [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="36796-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="36796-113">Lembre-se de que a interface **ITableData** não suporta as notificações de tabela para clientes que têm chamado **ScInitMapiUtil** em vez de **MAPIInitialize**.</span><span class="sxs-lookup"><span data-stu-id="36796-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  

