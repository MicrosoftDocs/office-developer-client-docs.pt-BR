---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a9b11b134f5d4a32a5a55008f557821d74b474bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357124"
---
# <a name="mapiofflinecreateinfo"></a><span data-ttu-id="9c600-103">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="9c600-103">MAPIOFFLINE_CREATEINFO</span></span>

  
  
<span data-ttu-id="9c600-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c600-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c600-105">Essa estrutura é usada com o [HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="9c600-105">This structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span>
  
```cpp
typedef struct
{
  ULONG      ulSize;
  ULONG      ulCreateFlags;
  LPCWSTR      pwszProfileName;
  ULONG      ulCapabilities;
  const GUID*      pGUID;
  const GUID*      pInstance;
  IMAPIOfflineMgr*    pParent;
  IUnknown*      pMAPISupport;
  MAPIOFFLINE_AGGREGATEINFO*  pAggregateInfo;
  MAPIOFFLINE_CONNECTINFO*  pConnectInfo;
} MAPIOFFLINE_CREATEINFO;
```

## <a name="members"></a><span data-ttu-id="9c600-106">Members</span><span class="sxs-lookup"><span data-stu-id="9c600-106">Members</span></span>

 <span data-ttu-id="9c600-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="9c600-107">**ulSize**</span></span>
  
> <span data-ttu-id="9c600-108">O tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="9c600-108">The size of structure.</span></span>
    
 <span data-ttu-id="9c600-109">**ulCreateFlags**</span><span class="sxs-lookup"><span data-stu-id="9c600-109">**ulCreateFlags**</span></span>
  
> <span data-ttu-id="9c600-110">Deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="9c600-110">It must be 0.</span></span>
    
 <span data-ttu-id="9c600-111">**pwszProfileName**</span><span class="sxs-lookup"><span data-stu-id="9c600-111">**pwszProfileName**</span></span>
  
> <span data-ttu-id="9c600-112">O nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="9c600-112">The name of the profile.</span></span>
    
 <span data-ttu-id="9c600-113">**ulCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9c600-113">**ulCapabilities**</span></span>
  
> <span data-ttu-id="9c600-114">Uma máscara de bits dos seguintes sinalizadores de recurso.</span><span class="sxs-lookup"><span data-stu-id="9c600-114">A bit mask of the following capability flags.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="9c600-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="9c600-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="9c600-116">O objeto offline é capaz de ficar offline.</span><span class="sxs-lookup"><span data-stu-id="9c600-116">The offline object is capable of going offline.</span></span>  <br/> |
|<span data-ttu-id="9c600-117">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="9c600-117">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="9c600-118">O objeto offline é capaz de entrar online.</span><span class="sxs-lookup"><span data-stu-id="9c600-118">The offline object is capable of going online.</span></span>  <br/> |
   
 <span data-ttu-id="9c600-119">**pGUID**</span><span class="sxs-lookup"><span data-stu-id="9c600-119">**pGUID**</span></span>
  
> <span data-ttu-id="9c600-120">Ponteiro para um GUID que é usado para identificar exclusivamente esse tipo de objeto offline de outros objetos offline.</span><span class="sxs-lookup"><span data-stu-id="9c600-120">Pointer to a GUID that is used to uniquely identify this type of offline object from other offline objects.</span></span> <span data-ttu-id="9c600-121">GUID_GlobalState refere-se ao objeto offline global que os objetos podem usar como um objeto pai.</span><span class="sxs-lookup"><span data-stu-id="9c600-121">GUID_GlobalState refers to the global offline object that objects can use as a parent object.</span></span>
    
 <span data-ttu-id="9c600-122">**pInstance**</span><span class="sxs-lookup"><span data-stu-id="9c600-122">**pInstance**</span></span>
  
> <span data-ttu-id="9c600-123">Ponteiro para o GUID que identifica exclusivamente este objeto offline.</span><span class="sxs-lookup"><span data-stu-id="9c600-123">Pointer to GUID that uniquely identifies this offline object.</span></span> <span data-ttu-id="9c600-124">Ela é usada para desambiguar esses objetos offline de outros objetos.</span><span class="sxs-lookup"><span data-stu-id="9c600-124">It is used to disambiguate this offline objects from other objects.</span></span>
    
 <span data-ttu-id="9c600-125">**pParent**</span><span class="sxs-lookup"><span data-stu-id="9c600-125">**pParent**</span></span>
  
> <span data-ttu-id="9c600-126">Ponteiro para objeto offline que é o pai deste objeto offline e cujas alterações esse objeto offline herdará.</span><span class="sxs-lookup"><span data-stu-id="9c600-126">Pointer to offline object that is the parent of this offline object and whose changes this offline object will inherit.</span></span>
    
 <span data-ttu-id="9c600-127">**pMAPISupport**</span><span class="sxs-lookup"><span data-stu-id="9c600-127">**pMAPISupport**</span></span>
  
>  <span data-ttu-id="9c600-128">Identifica o objeto de suporte MAPI que usará este objeto offline.</span><span class="sxs-lookup"><span data-stu-id="9c600-128">Identifies the MAPI support object that that will use this offline object.</span></span> <span data-ttu-id="9c600-129">Por exemplo, se este objeto offline é usado para controlar o estado offline e online de um repositório, este é o objeto de suporte de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c600-129">For example, if this offline object is used to keep track of a store's offline and online state, then this is the stores support object.</span></span> <span data-ttu-id="9c600-130">No enTanto, se este for um objeto offline para um objeto sem nenhum objeto support, ele poderá ser nulo.</span><span class="sxs-lookup"><span data-stu-id="9c600-130">However, if this is an offline object for an object with no support object then it can be NULL.</span></span> 
    
 <span data-ttu-id="9c600-131">**pAggregateInfo**</span><span class="sxs-lookup"><span data-stu-id="9c600-131">**pAggregateInfo**</span></span>
  
> <span data-ttu-id="9c600-132">Um ponteiro para uma estrutura MAPIOFFLINE_AGGREGATEINFO.</span><span class="sxs-lookup"><span data-stu-id="9c600-132">A pointer to a MAPIOFFLINE_AGGREGATEINFO structure.</span></span> <span data-ttu-id="9c600-133">Para obter mais informações, consulte [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span><span class="sxs-lookup"><span data-stu-id="9c600-133">For more information, see [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span></span>
    
 <span data-ttu-id="9c600-134">**pConnectInfo**</span><span class="sxs-lookup"><span data-stu-id="9c600-134">**pConnectInfo**</span></span>
  
> <span data-ttu-id="9c600-135">Deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="9c600-135">Must be null.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9c600-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c600-136">See also</span></span>



[<span data-ttu-id="9c600-137">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="9c600-137">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="9c600-138">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="9c600-138">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)

