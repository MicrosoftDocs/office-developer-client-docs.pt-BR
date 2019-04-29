---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Esse método foi preterido no Outlook Social Connector 2013.
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406889"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="c009f-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="c009f-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="c009f-104">Esse método foi preterido no Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="c009f-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="c009f-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="c009f-105">Remarks</span></span>

<span data-ttu-id="c009f-106">A partir do Outlook Social Connector 2013, o OSC oferece suporte apenas à sincronização sob demanda de atividades e não em cache ou sincronização híbrida de atividades.</span><span class="sxs-lookup"><span data-stu-id="c009f-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="c009f-107">O OSC ignora a configuração **cacheActivities** no XML Capabilities e não chama mais este método.</span><span class="sxs-lookup"><span data-stu-id="c009f-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="c009f-108">Para dar suporte à pesquisa de atividades dinâmicas, implemente o método [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="c009f-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="c009f-109">Defina \*\*\*\* getactivitiess **e dynamicActivitiesLookupEx** como **true**, que solicitará que o OSC chame **ISocialSession2:: GetActivitiesEx** em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c009f-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="c009f-110">Para obter mais informações sobre como o OSC Obtém as atividades dos amigos, confira [sincronizaNdo amigos e atividades](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="c009f-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c009f-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="c009f-111">See also</span></span>

- [<span data-ttu-id="c009f-112">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="c009f-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

