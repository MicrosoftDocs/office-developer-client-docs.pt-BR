---
title: GUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GUID
api_type:
- COM
ms.assetid: e3608c47-06be-4476-a6ef-060fac252387
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 12c50ab5936d7fffd364c276ba07ca69d3459ae7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421582"
---
# <a name="guid"></a><span data-ttu-id="ee8ed-103">GUID</span><span class="sxs-lookup"><span data-stu-id="ee8ed-103">GUID</span></span>

  
  
<span data-ttu-id="ee8ed-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee8ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee8ed-105">Descreve um identificador global exclusivo (GUID).</span><span class="sxs-lookup"><span data-stu-id="ee8ed-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee8ed-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ee8ed-106">Header file:</span></span>  <br/> |<span data-ttu-id="ee8ed-107">Mapiguid.h</span><span class="sxs-lookup"><span data-stu-id="ee8ed-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="ee8ed-108">Members</span><span class="sxs-lookup"><span data-stu-id="ee8ed-108">Members</span></span>

 <span data-ttu-id="ee8ed-109">**Data1**</span><span class="sxs-lookup"><span data-stu-id="ee8ed-109">**Data1**</span></span>
  
> <span data-ttu-id="ee8ed-110">Um valor de dados inteiro longo não assinado.</span><span class="sxs-lookup"><span data-stu-id="ee8ed-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="ee8ed-111">**Data2**</span><span class="sxs-lookup"><span data-stu-id="ee8ed-111">**Data2**</span></span>
  
> <span data-ttu-id="ee8ed-112">Um valor de dados de inteiro curto não assinado.</span><span class="sxs-lookup"><span data-stu-id="ee8ed-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="ee8ed-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="ee8ed-113">**Data3**</span></span>
  
> <span data-ttu-id="ee8ed-114">Um valor de dados de inteiro curto não assinado.</span><span class="sxs-lookup"><span data-stu-id="ee8ed-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="ee8ed-115">**Data4**</span><span class="sxs-lookup"><span data-stu-id="ee8ed-115">**Data4**</span></span>
  
> <span data-ttu-id="ee8ed-116">Uma matriz de caracteres não assinados.</span><span class="sxs-lookup"><span data-stu-id="ee8ed-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee8ed-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee8ed-117">Remarks</span></span>

 <span data-ttu-id="ee8ed-118">**Estruturas GUID** são usadas em MAPI da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="ee8ed-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="ee8ed-119">Nas [estruturas MAPIUID](mapiuid.md) que identificam exclusivamente provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="ee8ed-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="ee8ed-120">Para identificadores de interface.</span><span class="sxs-lookup"><span data-stu-id="ee8ed-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="ee8ed-121">Nos nomes de conjunto de propriedades de propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="ee8ed-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="ee8ed-122">Os provedores de armazenamento de mensagens e de agendas geram uma estrutura **GUID** a ser usada em **sua estrutura MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="ee8ed-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="ee8ed-123">Ao passar o **MAPIUID** resultante para [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), esses provedores de serviços informam AO MAPI sobre seu identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ee8ed-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="ee8ed-124">Além disso, eles são usados na implementação da Chamada de Procedimento Remoto da Microsoft (RPC) e da ODL (Object Description Language).</span><span class="sxs-lookup"><span data-stu-id="ee8ed-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="ee8ed-125">Para obter mais informações sobre esses usos, consulte o Guia e referência do programador do  *Microsoft RPC*, Referência do programador *OLE*  e  *Inside OLE*, *Segunda Edição*  .</span><span class="sxs-lookup"><span data-stu-id="ee8ed-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="ee8ed-126">A **estrutura GUID** é definida na Referência do *programador do Win32.*</span><span class="sxs-lookup"><span data-stu-id="ee8ed-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="ee8ed-127">Valores específicos para **estruturas GUID** que são usadas em MAPI são definidos no arquivo de header MAPI Mapiguid.h.</span><span class="sxs-lookup"><span data-stu-id="ee8ed-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee8ed-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee8ed-128">See also</span></span>



[<span data-ttu-id="ee8ed-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ee8ed-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="ee8ed-130">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="ee8ed-130">MAPI Structures</span></span>](mapi-structures.md)

