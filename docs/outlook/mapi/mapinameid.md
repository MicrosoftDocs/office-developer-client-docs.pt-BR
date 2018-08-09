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
ms.openlocfilehash: c3a21e8a6e69cae9d8b757a60fe56d63e079b3ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767990"
---
# <a name="mapinameid"></a><span data-ttu-id="9c090-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="9c090-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="9c090-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9c090-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9c090-105">Descreve uma propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="9c090-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c090-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9c090-106">Header file:</span></span>  <br/> |<span data-ttu-id="9c090-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c090-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="9c090-108">Members</span><span class="sxs-lookup"><span data-stu-id="9c090-108">Members</span></span>

 <span data-ttu-id="9c090-109">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="9c090-109">**lpguid**</span></span>
  
> <span data-ttu-id="9c090-110">Ponteiro para uma estrutura [GUID](guid.md) definindo uma determinada propriedade definido; Este membro não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="9c090-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="9c090-111">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="9c090-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="9c090-112">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="9c090-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="9c090-113">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="9c090-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="9c090-114">Um valor definido pelo cliente</span><span class="sxs-lookup"><span data-stu-id="9c090-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="9c090-115">**ulKind**</span><span class="sxs-lookup"><span data-stu-id="9c090-115">**ulKind**</span></span>
  
> <span data-ttu-id="9c090-116">Descrevendo o tipo de valor no membro do **tipo** de valor.</span><span class="sxs-lookup"><span data-stu-id="9c090-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="9c090-117">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="9c090-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="9c090-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="9c090-118">MNID_ID</span></span> 
  
> <span data-ttu-id="9c090-119">O **tipo** de membro contém um valor integer que representa o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="9c090-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="9c090-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="9c090-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="9c090-121">O **tipo** de membro contém uma cadeia de caracteres Unicode que representa o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="9c090-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="9c090-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9c090-122">**Kind**</span></span>
  
> <span data-ttu-id="9c090-123">União descrevendo o nome da propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="9c090-123">Union describing the name of the named property.</span></span> <span data-ttu-id="9c090-124">O nome pode ser um valor inteiro, armazenados em **lID**, ou uma cadeia de caracteres Unicode, armazenado em **lpwstrName**.</span><span class="sxs-lookup"><span data-stu-id="9c090-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c090-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c090-125">Remarks</span></span>

<span data-ttu-id="9c090-126">A estrutura **MAPINAMEID** é usada para descrever as propriedades de propriedades nomeadas que têm identificadores 0x8000 acima.</span><span class="sxs-lookup"><span data-stu-id="9c090-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="9c090-127">Um conjunto de propriedades é uma parte importante de uma propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="9c090-127">A property set is an important part a named property.</span></span> <span data-ttu-id="9c090-128">Por exemplo, PS_PUBLIC_STRINGS ou PS_ROUTING_ADDRTYPE são conjuntos de propriedades definidos pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="9c090-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="9c090-129">Propriedades nomeadas permitem que os clientes definir propriedades personalizadas em um namespace maior que o disponíveis no intervalo de identificador de propriedade definida pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="9c090-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="9c090-130">Os nomes de propriedade não podem ser usados para obter valores de propriedade diretamente; eles primeiro devem ser mapeados para os identificadores de propriedade por meio do método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="9c090-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="9c090-131">Para objetos específicos, como mensagens, MAPI reserva um intervalo de identificadores de propriedade de propriedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="9c090-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="9c090-132">Portanto, para esses objetos, clientes não precisam usar propriedades nomeadas e pode salvar o associado sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="9c090-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="9c090-133">Para obter mais informações sobre propriedades nomeadas, consulte [Propriedades chamado](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="9c090-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9c090-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c090-134">See also</span></span>



[<span data-ttu-id="9c090-135">GUID</span><span class="sxs-lookup"><span data-stu-id="9c090-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="9c090-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="9c090-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="9c090-137">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="9c090-137">MAPI Structures</span></span>](mapi-structures.md)

