---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Esse método foi preterido no Outlook Social Connector 2013.
ms.openlocfilehash: abad4fc2a3e3aaea8a7097ac7e6f56b0aadae299
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286161"
---
# <a name="isocialpersongetactivities"></a><span data-ttu-id="9722a-103">ISocialPerson::GetActivities</span><span class="sxs-lookup"><span data-stu-id="9722a-103">ISocialPerson::GetActivities</span></span>

<span data-ttu-id="9722a-104">Esse método foi preterido no Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="9722a-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a><span data-ttu-id="9722a-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="9722a-105">Remarks</span></span>

<span data-ttu-id="9722a-106">A partir do Outlook Social Connector 2013, o OSC oferece suporte apenas à sincronização sob demanda de atividades e não em cache ou sincronização híbrida de atividades.</span><span class="sxs-lookup"><span data-stu-id="9722a-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="9722a-107">O OSC ignora a configuração **cacheActivities** no XML Capabilities e não chama esse método.</span><span class="sxs-lookup"><span data-stu-id="9722a-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and does not call this method.</span></span> <span data-ttu-id="9722a-108">Para dar suporte à pesquisa de atividades dinâmicas, implemente o método [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="9722a-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="9722a-109">Defina **cacheActivities** como **false**, **getactivities** e **dynamicActivitiesLookupEx** como **true**, que solicitará que o OSC chame **ISocialSession2:: GetActivitiesEx** em vez disso.</span><span class="sxs-lookup"><span data-stu-id="9722a-109">Set **cacheActivities** as **false**, **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="9722a-110">Para obter mais informações sobre como o OSC Obtém as atividades dos amigos, confira [sincronizaNdo amigos e atividades](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="9722a-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9722a-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="9722a-111">See also</span></span>

- [<span data-ttu-id="9722a-112">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9722a-112">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

