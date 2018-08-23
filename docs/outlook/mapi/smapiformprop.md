---
title: SMAPIFormProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormProp
api_type:
- COM
ms.assetid: 80f1c2e0-3567-4b16-86cb-d5e6ac95c2ee
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4e8e2474d2adb882dd0ba43aeb0d8b05044a6ce6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592056"
---
# <a name="smapiformprop"></a><span data-ttu-id="d49bf-103">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="d49bf-103">SMAPIFormProp</span></span>

  
  
<span data-ttu-id="d49bf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d49bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d49bf-105">Descreve uma propriedade nomeada utilizada com um formulário.</span><span class="sxs-lookup"><span data-stu-id="d49bf-105">Describes a named property used with a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d49bf-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d49bf-106">Header file:</span></span>  <br/> |<span data-ttu-id="d49bf-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="d49bf-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormProp
{
  ULONG ulFlags;
  ULONG nPropType;
  MAPINAMEID nmid;
  LPSTR pszDisplayName;
  FORMPROPSPECIALTYPE nSpecialType;
  union
  {
    struct
    {
      MAPINAMEID nmidIdx;
      ULONG cfpevAvailable;
      LPMAPIFORMPROPENUMVAL pfpevAvailable;
    } s1;
  } u;
} SMAPIFormProp, FAR * LPMAPIFORMPROP;

```

## <a name="members"></a><span data-ttu-id="d49bf-108">Members</span><span class="sxs-lookup"><span data-stu-id="d49bf-108">Members</span></span>

 <span data-ttu-id="d49bf-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="d49bf-109">**ulFlags**</span></span>
  
> <span data-ttu-id="d49bf-110">Sinalizadores usados para distinguir o formato das cadeias de caracteres na estrutura **SMAPIFormProp** .</span><span class="sxs-lookup"><span data-stu-id="d49bf-110">Flags used to distinguish the format of the strings in the **SMAPIFormProp** structure.</span></span> <span data-ttu-id="d49bf-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="d49bf-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="d49bf-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d49bf-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d49bf-113">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d49bf-113">The strings returned are in Unicode format.</span></span> <span data-ttu-id="d49bf-114">Se MAPI_UNICODE não estiver definida, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d49bf-114">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d49bf-115">**nPropType**</span><span class="sxs-lookup"><span data-stu-id="d49bf-115">**nPropType**</span></span>
  
> <span data-ttu-id="d49bf-116">Tipo da propriedade nomeado, com a palavra mais significativa definida como zero.</span><span class="sxs-lookup"><span data-stu-id="d49bf-116">Type of the named property, with the most significant word set to zero.</span></span> 
    
 <span data-ttu-id="d49bf-117">**nmid**</span><span class="sxs-lookup"><span data-stu-id="d49bf-117">**nmid**</span></span>
  
> <span data-ttu-id="d49bf-118">Nome da propriedade nomeada, que inclui uma estrutura **GUID** que identifica o valor da propriedade set e um numérico ou cadeia de caracteres que representa um nome de formulário e de identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="d49bf-118">Name for the named property, which includes a **GUID** structure identifying the property set and either a numeric or string value that represents an interface identifier and form name.</span></span> 
    
 <span data-ttu-id="d49bf-119">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="d49bf-119">**pszDisplayName**</span></span>
  
> <span data-ttu-id="d49bf-120">Ponteiro para o nome para exibição da propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="d49bf-120">Pointer to the display name of the named property.</span></span>
    
 <span data-ttu-id="d49bf-121">**nSpecialType**</span><span class="sxs-lookup"><span data-stu-id="d49bf-121">**nSpecialType**</span></span>
  
> <span data-ttu-id="d49bf-122">Valor que descreve o tipo de dados incluídos no membro **u** .</span><span class="sxs-lookup"><span data-stu-id="d49bf-122">Value describing the type of data included in the **u** member.</span></span> <span data-ttu-id="d49bf-123">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="d49bf-123">Possible values are as follows:</span></span> 
    
<span data-ttu-id="d49bf-124">FPST_VANILLA</span><span class="sxs-lookup"><span data-stu-id="d49bf-124">FPST_VANILLA</span></span> 
  
> <span data-ttu-id="d49bf-125">O membro **u** não contiver uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="d49bf-125">The **u** member does not contain an enumeration.</span></span> 
    
<span data-ttu-id="d49bf-126">FPST_ENUM_PROP</span><span class="sxs-lookup"><span data-stu-id="d49bf-126">FPST_ENUM_PROP</span></span> 
  
> <span data-ttu-id="d49bf-127">O membro **u** contém uma estrutura que descreve uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="d49bf-127">The **u** member contains a structure that describes an enumeration.</span></span> 
    
 <span data-ttu-id="d49bf-128">**u**</span><span class="sxs-lookup"><span data-stu-id="d49bf-128">**u**</span></span>
  
> <span data-ttu-id="d49bf-129">União descrevendo a associação entre o nome e o número da propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="d49bf-129">Union describing the association between the name and number of the named property.</span></span> <span data-ttu-id="d49bf-130">Usando algumas propriedades, o membro **u** está vazio.</span><span class="sxs-lookup"><span data-stu-id="d49bf-130">By using some properties, the **u** member is empty.</span></span> <span data-ttu-id="d49bf-131">Com outras propriedades, ele é representado em uma estrutura que consiste dos seguintes membros:</span><span class="sxs-lookup"><span data-stu-id="d49bf-131">With other properties, it is represented in a structure consisting of the following members:</span></span> 
    
 <span data-ttu-id="d49bf-132">**nmidIdx**</span><span class="sxs-lookup"><span data-stu-id="d49bf-132">**nmidIdx**</span></span>
  
> <span data-ttu-id="d49bf-133">A estrutura [MAPINAMEID](mapinameid.md) que contém o conjunto de propriedades e o identificador para a propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="d49bf-133">The [MAPINAMEID](mapinameid.md) structure that contains the property set and identifier for the named property.</span></span> 
    
 <span data-ttu-id="d49bf-134">**cfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="d49bf-134">**cfpevAvailable**</span></span>
  
> <span data-ttu-id="d49bf-135">Contagem de estruturas de [SMAPIFormPropEnumVal](smapiformpropenumval.md) na matriz apontado pelo membro **pfpevAvailable** .</span><span class="sxs-lookup"><span data-stu-id="d49bf-135">Count of [SMAPIFormPropEnumVal](smapiformpropenumval.md) structures in the array pointed to by the **pfpevAvailable** member.</span></span> 
    
 <span data-ttu-id="d49bf-136">**pfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="d49bf-136">**pfpevAvailable**</span></span>
  
> <span data-ttu-id="d49bf-137">Ponteiro para uma matriz de estruturas de **SMAPIFormPropEnumVal** , cada um dos quais mantém um valor para a propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="d49bf-137">Pointer to an array of **SMAPIFormPropEnumVal** structures, each of which holds a value for the named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d49bf-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="d49bf-138">Remarks</span></span>

<span data-ttu-id="d49bf-139">A estrutura de **SMAPIFormProp** contém informações sobre uma propriedade de formulário usada como parte das definições de interface do [IMAPIFormInfo](imapiforminfoimapiprop.md) ; **nSpecialType** contém uma marca que se aplica a união **u** que faz parte do **SMAPIFormProp**.</span><span class="sxs-lookup"><span data-stu-id="d49bf-139">The **SMAPIFormProp** structure contains information about a form property used as part of the definitions of the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface; **nSpecialType** contains a tag that applies to the **u** union that is part of **SMAPIFormProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d49bf-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="d49bf-140">See also</span></span>



[<span data-ttu-id="d49bf-141">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="d49bf-141">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="d49bf-142">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="d49bf-142">SMAPIFormPropEnumVal</span></span>](smapiformpropenumval.md)


[<span data-ttu-id="d49bf-143">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="d49bf-143">MAPI Structures</span></span>](mapi-structures.md)

