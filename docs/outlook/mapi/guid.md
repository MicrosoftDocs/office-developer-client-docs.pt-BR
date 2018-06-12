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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 08ecb718572944db07c2888e0aae1464bd5c0f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766670"
---
# <a name="guid"></a><span data-ttu-id="c4092-103">GUID</span><span class="sxs-lookup"><span data-stu-id="c4092-103">GUID</span></span>

  
  
<span data-ttu-id="c4092-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4092-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c4092-105">Descreve um identificador global exclusivo (GUID).</span><span class="sxs-lookup"><span data-stu-id="c4092-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4092-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c4092-106">Header file:</span></span>  <br/> |<span data-ttu-id="c4092-107">Mapiguid.h</span><span class="sxs-lookup"><span data-stu-id="c4092-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="c4092-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c4092-108">Members</span></span>

 <span data-ttu-id="c4092-109">**Data1**</span><span class="sxs-lookup"><span data-stu-id="c4092-109">**Data1**</span></span>
  
> <span data-ttu-id="c4092-110">Um valor de dados de inteiro longo não assinado.</span><span class="sxs-lookup"><span data-stu-id="c4092-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="c4092-111">**Data2**</span><span class="sxs-lookup"><span data-stu-id="c4092-111">**Data2**</span></span>
  
> <span data-ttu-id="c4092-112">Um valor de dados de inteiro não assinado de curta.</span><span class="sxs-lookup"><span data-stu-id="c4092-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="c4092-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="c4092-113">**Data3**</span></span>
  
> <span data-ttu-id="c4092-114">Um valor de dados de inteiro não assinado de curta.</span><span class="sxs-lookup"><span data-stu-id="c4092-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="c4092-115">**Data4**</span><span class="sxs-lookup"><span data-stu-id="c4092-115">**Data4**</span></span>
  
> <span data-ttu-id="c4092-116">Uma matriz de caracteres não assinados.</span><span class="sxs-lookup"><span data-stu-id="c4092-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c4092-117">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="c4092-117">Remarks</span></span>

 <span data-ttu-id="c4092-118">Estruturas **GUID** são usadas na MAPI, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c4092-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="c4092-119">Nas estruturas [MAPIUID](mapiuid.md) que identificam exclusivamente os provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="c4092-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="c4092-120">Para os identificadores de interface.</span><span class="sxs-lookup"><span data-stu-id="c4092-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="c4092-121">Na propriedade define nomes de propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="c4092-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="c4092-122">Armazenamento de mensagens e o endereço de provedores de catálogo geram uma estrutura **GUID** para usar em sua estrutura **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="c4092-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="c4092-123">Passando o resultante **MAPIUID** para [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), esses provedores de serviço informam MAPI do seu identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c4092-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="c4092-124">Além disso, eles são usados na implementação do Microsoft Remote Procedure Call (RPC) e o idioma de descrição de objeto (ODL).</span><span class="sxs-lookup"><span data-stu-id="c4092-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="c4092-125">Para obter mais informações sobre esses usos, consulte o *Guia do programador do Microsoft RPC e referência*, *referência do programador do OLE* e *Dentro OLE*, *Second Edition* .</span><span class="sxs-lookup"><span data-stu-id="c4092-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="c4092-126">A estrutura **GUID** é definida na *referência do programador do Win32* .</span><span class="sxs-lookup"><span data-stu-id="c4092-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="c4092-127">Valores específicos para estruturas **GUID** que são usados em MAPI são definidos no arquivo de cabeçalho MAPI Mapiguid.h.</span><span class="sxs-lookup"><span data-stu-id="c4092-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c4092-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4092-128">See also</span></span>



[<span data-ttu-id="c4092-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="c4092-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="c4092-130">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="c4092-130">MAPI Structures</span></span>](mapi-structures.md)

