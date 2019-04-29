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
ms.openlocfilehash: 968f9e1dad3a233b31f0ce29d3ce935b1257948c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416696"
---
# <a name="smapiformprop"></a><span data-ttu-id="bb751-103">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="bb751-103">SMAPIFormProp</span></span>

  
  
<span data-ttu-id="bb751-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb751-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb751-105">Descreve uma propriedade nomeada usada com um formulário.</span><span class="sxs-lookup"><span data-stu-id="bb751-105">Describes a named property used with a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb751-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="bb751-106">Header file:</span></span>  <br/> |<span data-ttu-id="bb751-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="bb751-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="bb751-108">Membros</span><span class="sxs-lookup"><span data-stu-id="bb751-108">Members</span></span>

 <span data-ttu-id="bb751-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="bb751-109">**ulFlags**</span></span>
  
> <span data-ttu-id="bb751-110">Sinalizadores usados para distinguir o formato das cadeias de caracteres na estrutura **SMAPIFormProp** .</span><span class="sxs-lookup"><span data-stu-id="bb751-110">Flags used to distinguish the format of the strings in the **SMAPIFormProp** structure.</span></span> <span data-ttu-id="bb751-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="bb751-111">The following flag can be set:</span></span> 
    
<span data-ttu-id="bb751-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bb751-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bb751-113">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="bb751-113">The strings returned are in Unicode format.</span></span> <span data-ttu-id="bb751-114">Se MAPI_UNICODE não for definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="bb751-114">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="bb751-115">**nPropType**</span><span class="sxs-lookup"><span data-stu-id="bb751-115">**nPropType**</span></span>
  
> <span data-ttu-id="bb751-116">Tipo da propriedade nomeada, com a palavra mais significativa definida como zero.</span><span class="sxs-lookup"><span data-stu-id="bb751-116">Type of the named property, with the most significant word set to zero.</span></span> 
    
 <span data-ttu-id="bb751-117">**nmid**</span><span class="sxs-lookup"><span data-stu-id="bb751-117">**nmid**</span></span>
  
> <span data-ttu-id="bb751-118">Nome da propriedade nomeada, que inclui uma estrutura **GUID** que identifica o conjunto de propriedades e um valor numérico ou de cadeia de caracteres que representa um identificador de interface e um nome de formulário.</span><span class="sxs-lookup"><span data-stu-id="bb751-118">Name for the named property, which includes a **GUID** structure identifying the property set and either a numeric or string value that represents an interface identifier and form name.</span></span> 
    
 <span data-ttu-id="bb751-119">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="bb751-119">**pszDisplayName**</span></span>
  
> <span data-ttu-id="bb751-120">Ponteiro para o nome de exibição da propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="bb751-120">Pointer to the display name of the named property.</span></span>
    
 <span data-ttu-id="bb751-121">**nSpecialType**</span><span class="sxs-lookup"><span data-stu-id="bb751-121">**nSpecialType**</span></span>
  
> <span data-ttu-id="bb751-122">Valor que descreve o tipo de dados incluído no membro **u** .</span><span class="sxs-lookup"><span data-stu-id="bb751-122">Value describing the type of data included in the **u** member.</span></span> <span data-ttu-id="bb751-123">Os valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="bb751-123">Possible values are as follows:</span></span> 
    
<span data-ttu-id="bb751-124">FPST_VANILLA</span><span class="sxs-lookup"><span data-stu-id="bb751-124">FPST_VANILLA</span></span> 
  
> <span data-ttu-id="bb751-125">O membro **u** não contém uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="bb751-125">The **u** member does not contain an enumeration.</span></span> 
    
<span data-ttu-id="bb751-126">FPST_ENUM_PROP</span><span class="sxs-lookup"><span data-stu-id="bb751-126">FPST_ENUM_PROP</span></span> 
  
> <span data-ttu-id="bb751-127">O membro **u** contém uma estrutura que descreve uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="bb751-127">The **u** member contains a structure that describes an enumeration.</span></span> 
    
 <span data-ttu-id="bb751-128">**u**</span><span class="sxs-lookup"><span data-stu-id="bb751-128">**u**</span></span>
  
> <span data-ttu-id="bb751-129">União descrevendo a associação entre o nome e o número da propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="bb751-129">Union describing the association between the name and number of the named property.</span></span> <span data-ttu-id="bb751-130">Usando algumas propriedades, o membro **u** está vazio.</span><span class="sxs-lookup"><span data-stu-id="bb751-130">By using some properties, the **u** member is empty.</span></span> <span data-ttu-id="bb751-131">Com outras propriedades, ela é representada em uma estrutura que consiste nos seguintes membros:</span><span class="sxs-lookup"><span data-stu-id="bb751-131">With other properties, it is represented in a structure consisting of the following members:</span></span> 
    
 <span data-ttu-id="bb751-132">**nmidIdx**</span><span class="sxs-lookup"><span data-stu-id="bb751-132">**nmidIdx**</span></span>
  
> <span data-ttu-id="bb751-133">A estrutura [MAPINAMEID](mapinameid.md) que contém o conjunto de propriedades e o identificador da propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="bb751-133">The [MAPINAMEID](mapinameid.md) structure that contains the property set and identifier for the named property.</span></span> 
    
 <span data-ttu-id="bb751-134">**cfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="bb751-134">**cfpevAvailable**</span></span>
  
> <span data-ttu-id="bb751-135">Contagem de estruturas [SMAPIFormPropEnumVal](smapiformpropenumval.md) na matriz apontada pelo membro **pfpevAvailable** .</span><span class="sxs-lookup"><span data-stu-id="bb751-135">Count of [SMAPIFormPropEnumVal](smapiformpropenumval.md) structures in the array pointed to by the **pfpevAvailable** member.</span></span> 
    
 <span data-ttu-id="bb751-136">**pfpevAvailable**</span><span class="sxs-lookup"><span data-stu-id="bb751-136">**pfpevAvailable**</span></span>
  
> <span data-ttu-id="bb751-137">Ponteiro para uma matriz de estruturas **SMAPIFormPropEnumVal** , cada uma delas armazena um valor para a propriedade named.</span><span class="sxs-lookup"><span data-stu-id="bb751-137">Pointer to an array of **SMAPIFormPropEnumVal** structures, each of which holds a value for the named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bb751-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb751-138">Remarks</span></span>

<span data-ttu-id="bb751-139">A estrutura **SMAPIFormProp** contém informações sobre uma propriedade de formulário usada como parte das definições da interface [IMAPIFormInfo](imapiforminfoimapiprop.md) ; **nSpecialType** contém uma marca que se aplica à União **u** que faz parte de **SMAPIFormProp**.</span><span class="sxs-lookup"><span data-stu-id="bb751-139">The **SMAPIFormProp** structure contains information about a form property used as part of the definitions of the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface; **nSpecialType** contains a tag that applies to the **u** union that is part of **SMAPIFormProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bb751-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb751-140">See also</span></span>



[<span data-ttu-id="bb751-141">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="bb751-141">MAPINAMEID</span></span>](mapinameid.md)
  
[<span data-ttu-id="bb751-142">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="bb751-142">SMAPIFormPropEnumVal</span></span>](smapiformpropenumval.md)


[<span data-ttu-id="bb751-143">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="bb751-143">MAPI Structures</span></span>](mapi-structures.md)

