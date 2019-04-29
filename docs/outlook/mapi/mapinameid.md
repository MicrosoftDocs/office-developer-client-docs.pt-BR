---
title: MAPINAMEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPINAMEID
api_type:
- COM
ms.assetid: 9a92e9cd-8282-4cf0-93af-4089b3763594
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: baec750a460b3ba9becd2e1dddf967705424ac4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411677"
---
# <a name="mapinameid"></a><span data-ttu-id="df204-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="df204-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="df204-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df204-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df204-105">Descreve uma propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="df204-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df204-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="df204-106">Header file:</span></span>  <br/> |<span data-ttu-id="df204-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="df204-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _MAPINAMEID
{
  LPGUID lpguid;
  ULONG ulKind;
  union
  {
    LONG lID;
    LPWSTR lpwstrName;
  } Kind;
} MAPINAMEID, FAR *LPMAPINAMEID;

```

## <a name="members"></a><span data-ttu-id="df204-108">Members</span><span class="sxs-lookup"><span data-stu-id="df204-108">Members</span></span>

 <span data-ttu-id="df204-109">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="df204-109">**lpguid**</span></span>
  
> <span data-ttu-id="df204-110">Ponteiro para uma estrutura [GUID](guid.md) que define um determinado conjunto de propriedades; Este membro não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="df204-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="df204-111">Os valores válidos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="df204-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="df204-112">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="df204-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="df204-113">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="df204-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="df204-114">Um valor definido pelo cliente</span><span class="sxs-lookup"><span data-stu-id="df204-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="df204-115">**Uikindda**</span><span class="sxs-lookup"><span data-stu-id="df204-115">**ulKind**</span></span>
  
> <span data-ttu-id="df204-116">Valor que descreve o tipo de valor no membro do **tipo** .</span><span class="sxs-lookup"><span data-stu-id="df204-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="df204-117">Os valores válidos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="df204-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="df204-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="df204-118">MNID_ID</span></span> 
  
> <span data-ttu-id="df204-119">O **tipo** membro contém um valor inteiro que representa o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="df204-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="df204-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="df204-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="df204-121">O **tipo** member contém uma cadeia de caracteres Unicode que representa o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="df204-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="df204-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="df204-122">**Kind**</span></span>
  
> <span data-ttu-id="df204-123">União descrevendo o nome da propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="df204-123">Union describing the name of the named property.</span></span> <span data-ttu-id="df204-124">O nome pode ser um valor inteiro, armazenado em **tampa**ou uma cadeia de caracteres Unicode, armazenado em **lpwstrName**.</span><span class="sxs-lookup"><span data-stu-id="df204-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df204-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="df204-125">Remarks</span></span>

<span data-ttu-id="df204-126">A estrutura **MAPINAMEID** é usada para descrever propriedades nomeadas propriedades que têm identificadores sobre 0x8000.</span><span class="sxs-lookup"><span data-stu-id="df204-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="df204-127">Um conjunto de propriedades é uma parte importante de uma propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="df204-127">A property set is an important part a named property.</span></span> <span data-ttu-id="df204-128">Por exemplo, PS_PUBLIC_STRINGS ou PS_ROUTING_ADDRTYPE são conjuntos de propriedades definidos por MAPI.</span><span class="sxs-lookup"><span data-stu-id="df204-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="df204-129">As propriedades nomeadas permitem que os clientes definam Propriedades personalizadas em um namespace maior do que o disponível no intervalo de identificador de propriedade definida por MAPI.</span><span class="sxs-lookup"><span data-stu-id="df204-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="df204-130">Os nomes de propriedade não podem ser usados para obter valores de propriedade diretamente; Eles devem ser mapeados primeiro para os identificadores de propriedade por meio do método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="df204-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="df204-131">Para determinados objetos como mensagens, MAPI reserva um intervalo de identificadores de propriedade para propriedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="df204-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="df204-132">Portanto, para esses objetos, os clientes não precisam usar propriedades nomeadas e podem salvar a sobrecarga associada.</span><span class="sxs-lookup"><span data-stu-id="df204-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="df204-133">Para obter mais informações sobre propriedades nomeadas, consulte [propriedades nomeadas](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="df204-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="df204-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="df204-134">See also</span></span>



[<span data-ttu-id="df204-135">GUID</span><span class="sxs-lookup"><span data-stu-id="df204-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="df204-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="df204-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="df204-137">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="df204-137">MAPI Structures</span></span>](mapi-structures.md)

