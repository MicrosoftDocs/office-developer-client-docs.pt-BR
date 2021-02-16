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
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="67470-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="67470-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="67470-104">Esse método foi preterido no Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="67470-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="67470-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="67470-105">Remarks</span></span>

<span data-ttu-id="67470-106">A partir do Outlook Social Connector 2013, o OSC oferece suporte apenas à sincronização sob demanda de atividades e não sincronização híbrida ou em cache de atividades.</span><span class="sxs-lookup"><span data-stu-id="67470-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="67470-107">O OSC ignora a **configuração cacheActivities** no XML de recursos e não chama mais esse método.</span><span class="sxs-lookup"><span data-stu-id="67470-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="67470-108">Para dar suporte à pesquisa de atividades dinâmicas, implemente o método [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md)</span><span class="sxs-lookup"><span data-stu-id="67470-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="67470-109">Definir **getActivities** e **dynamicActivitiesLookupEx** como **true**, que solicitará que o OSC chame **ISocialSession2::GetActivitiesEx** em vez disso.</span><span class="sxs-lookup"><span data-stu-id="67470-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="67470-110">Para obter mais informações sobre como o OSC obtém atividades de amigos, consulte [Sincronizando amigos e atividades.](synchronizing-friends-and-activities.md)</span><span class="sxs-lookup"><span data-stu-id="67470-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="67470-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="67470-111">See also</span></span>

- [<span data-ttu-id="67470-112">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="67470-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

