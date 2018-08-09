---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Este método foi preterido no Outlook Social Connector 2013.
ms.openlocfilehash: 54b5cd6d681aa1e8008eade024ef57783bf18ead
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770870"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="e97e8-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="e97e8-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="e97e8-104">Este método foi preterido no Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="e97e8-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="e97e8-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="e97e8-105">Remarks</span></span>

<span data-ttu-id="e97e8-106">Iniciando no Outlook Social Connector 2013, o OSC suporta apenas sob demanda sincronização de atividades e não em cache ou sincronização híbrida das atividades.</span><span class="sxs-lookup"><span data-stu-id="e97e8-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="e97e8-107">O OSC ignora a configuração de **cacheActivities** nos recursos de XML e não são mais chama esse método.</span><span class="sxs-lookup"><span data-stu-id="e97e8-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="e97e8-108">Para dar suporte à pesquisa de atividades dinâmico, implemente o método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="e97e8-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="e97e8-109">Definir **getActivities** e **dynamicActivitiesLookupEx** como **true**, que solicitará que o OSC chamada **ISocialSession2::GetActivitiesEx** em vez disso.</span><span class="sxs-lookup"><span data-stu-id="e97e8-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="e97e8-110">Para obter mais informações sobre como o OSC obtém atividades dos amigos, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="e97e8-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e97e8-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="e97e8-111">See also</span></span>

- [<span data-ttu-id="e97e8-112">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="e97e8-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

