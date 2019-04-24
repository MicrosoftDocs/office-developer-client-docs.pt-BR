---
title: FLAGLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLAGLIST
api_type:
- COM
ms.assetid: b4c0655c-1a3a-4f89-a977-0431db596512
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a5e508f5f7e6554a115517da87a8eac39f39aecf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336936"
---
# <a name="flaglist"></a><span data-ttu-id="b80dd-103">FLAGLIST</span><span class="sxs-lookup"><span data-stu-id="b80dd-103">FLAGLIST</span></span>

  
  
<span data-ttu-id="b80dd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b80dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b80dd-105">Contém uma lista de sinalizadores usados para indicar o status das entradas de endereço durante o processo de resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="b80dd-105">Contains a list of flags used to indicate the status of address entries during the name resolution process.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b80dd-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b80dd-106">Header file:</span></span>  <br/> |<span data-ttu-id="b80dd-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b80dd-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a><span data-ttu-id="b80dd-108">Members</span><span class="sxs-lookup"><span data-stu-id="b80dd-108">Members</span></span>

 <span data-ttu-id="b80dd-109">**cFlags**</span><span class="sxs-lookup"><span data-stu-id="b80dd-109">**cFlags**</span></span>
  
> <span data-ttu-id="b80dd-110">Contagem de sinalizadores definidos por MAPI na lista.</span><span class="sxs-lookup"><span data-stu-id="b80dd-110">Count of MAPI-defined flags in the list.</span></span>
    
 <span data-ttu-id="b80dd-111">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="b80dd-111">**ulFlags**</span></span>
  
> <span data-ttu-id="b80dd-112">Uma matriz de sinalizadores que fornece o status da operação de resolução de nome de um destinatário.</span><span class="sxs-lookup"><span data-stu-id="b80dd-112">An array of flags that provides the status of the name resolution operation for a recipient.</span></span> <span data-ttu-id="b80dd-113">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="b80dd-113">The following flags can be set:</span></span>
    
<span data-ttu-id="b80dd-114">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="b80dd-114">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="b80dd-115">O destinatário foi resolvido, mas não a um identificador de entrada exclusivo.</span><span class="sxs-lookup"><span data-stu-id="b80dd-115">The recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="b80dd-116">Outros contêineres do catálogo de endereços não devem tentar resolver esse destinatário.</span><span class="sxs-lookup"><span data-stu-id="b80dd-116">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="b80dd-117">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="b80dd-117">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="b80dd-118">O destinatário foi resolvido para um identificador de entrada exclusivo.</span><span class="sxs-lookup"><span data-stu-id="b80dd-118">The recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="b80dd-119">Outros contêineres do catálogo de endereços não devem tentar resolver esse destinatário.</span><span class="sxs-lookup"><span data-stu-id="b80dd-119">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="b80dd-120">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="b80dd-120">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="b80dd-121">A entrada não foi resolvida.</span><span class="sxs-lookup"><span data-stu-id="b80dd-121">The entry has not been resolved.</span></span> <span data-ttu-id="b80dd-122">Outros contêineres do catálogo de endereços devem tentar resolver esse destinatário.</span><span class="sxs-lookup"><span data-stu-id="b80dd-122">Other address book containers should try to resolve this recipient.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b80dd-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b80dd-123">Remarks</span></span>

<span data-ttu-id="b80dd-124">A estrutura da **marca de sinalizador** é usada como um parâmetro para [IABContainer:: ResolveNames](iabcontainer-resolvenames.md).</span><span class="sxs-lookup"><span data-stu-id="b80dd-124">The **FLAGLIST** structure is used as a parameter to [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span></span> <span data-ttu-id="b80dd-125">Cada um dos destinatários a serem resolvidos está incluído em uma estrutura [das ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="b80dd-125">Each of the recipients to be resolved is included in an [ADRLIST](adrlist.md) structure.</span></span> <span data-ttu-id="b80dd-126">Como o contêiner de catálogo de endereços tenta resolver cada destinatário, ele define o sinalizador apropriado na entrada correspondente na estrutura **flaglist** .</span><span class="sxs-lookup"><span data-stu-id="b80dd-126">As the address book container attempts to resolve each recipient, it sets the appropriate flag in the corresponding entry in the **FLAGLIST** structure.</span></span> <span data-ttu-id="b80dd-127">Todas as entradas na estrutura **flaglist** estão na mesma ordem das entradas na estrutura **das ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="b80dd-127">All of the entries in the **FLAGLIST** structure are in the same order as the entries in the **ADRLIST** structure.</span></span> <span data-ttu-id="b80dd-128">Isso facilita a associação de uma configuração de sinalizador a um destinatário.</span><span class="sxs-lookup"><span data-stu-id="b80dd-128">This makes it easy to associate a flag setting with a recipient.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b80dd-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="b80dd-129">See also</span></span>



[<span data-ttu-id="b80dd-130">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="b80dd-130">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="b80dd-131">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="b80dd-131">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="b80dd-132">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="b80dd-132">MAPI Structures</span></span>](mapi-structures.md)

