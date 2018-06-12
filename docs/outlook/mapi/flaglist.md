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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 2cf5ff69e8453b2da26fd5044823ddf4f99a9f45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766566"
---
# <a name="flaglist"></a><span data-ttu-id="1ca12-103">FLAGLIST</span><span class="sxs-lookup"><span data-stu-id="1ca12-103">FLAGLIST</span></span>

  
  
<span data-ttu-id="1ca12-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ca12-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ca12-105">Contém uma lista dos sinalizadores usados para indicar o status das entradas de endereço durante o processo de resolução de nome.</span><span class="sxs-lookup"><span data-stu-id="1ca12-105">Contains a list of flags used to indicate the status of address entries during the name resolution process.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1ca12-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1ca12-106">Header file:</span></span>  <br/> |<span data-ttu-id="1ca12-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ca12-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a><span data-ttu-id="1ca12-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1ca12-108">Members</span></span>

 <span data-ttu-id="1ca12-109">**cFlags**</span><span class="sxs-lookup"><span data-stu-id="1ca12-109">**cFlags**</span></span>
  
> <span data-ttu-id="1ca12-110">Contagem de sinalizadores MAPI-definidos na lista.</span><span class="sxs-lookup"><span data-stu-id="1ca12-110">Count of MAPI-defined flags in the list.</span></span>
    
 <span data-ttu-id="1ca12-111">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="1ca12-111">**ulFlags**</span></span>
  
> <span data-ttu-id="1ca12-112">Uma matriz dos sinalizadores que fornece o status da operação de resolução de nome de um destinatário.</span><span class="sxs-lookup"><span data-stu-id="1ca12-112">An array of flags that provides the status of the name resolution operation for a recipient.</span></span> <span data-ttu-id="1ca12-113">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="1ca12-113">The following flags can be set:</span></span>
    
<span data-ttu-id="1ca12-114">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="1ca12-114">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="1ca12-115">O destinatário foi resolvido, mas não a um identificador exclusivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="1ca12-115">The recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="1ca12-116">Outros contêineres do catálogo de endereços não devem tentar resolver o destinatário.</span><span class="sxs-lookup"><span data-stu-id="1ca12-116">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="1ca12-117">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="1ca12-117">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="1ca12-118">O destinatário foi resolvido para um identificador exclusivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="1ca12-118">The recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="1ca12-119">Outros contêineres do catálogo de endereços não devem tentar resolver o destinatário.</span><span class="sxs-lookup"><span data-stu-id="1ca12-119">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="1ca12-120">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="1ca12-120">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="1ca12-121">A entrada não foi resolvida.</span><span class="sxs-lookup"><span data-stu-id="1ca12-121">The entry has not been resolved.</span></span> <span data-ttu-id="1ca12-122">Outros contêineres do catálogo de endereços devem tentar resolver o destinatário.</span><span class="sxs-lookup"><span data-stu-id="1ca12-122">Other address book containers should try to resolve this recipient.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ca12-123">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="1ca12-123">Remarks</span></span>

<span data-ttu-id="1ca12-124">A estrutura **FLAGLIST** é usada como um parâmetro para [IABContainer:: ResolveNames](iabcontainer-resolvenames.md).</span><span class="sxs-lookup"><span data-stu-id="1ca12-124">The **FLAGLIST** structure is used as a parameter to [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span></span> <span data-ttu-id="1ca12-125">Cada um dos destinatários ser resolvido está incluída em uma estrutura [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="1ca12-125">Each of the recipients to be resolved is included in an [ADRLIST](adrlist.md) structure.</span></span> <span data-ttu-id="1ca12-126">Como o contêiner de catálogo de endereços tenta resolver cada destinatário, ele define o sinalizador apropriado na entrada correspondente na estrutura **FLAGLIST** .</span><span class="sxs-lookup"><span data-stu-id="1ca12-126">As the address book container attempts to resolve each recipient, it sets the appropriate flag in the corresponding entry in the **FLAGLIST** structure.</span></span> <span data-ttu-id="1ca12-127">Todas as entradas na estrutura de **FLAGLIST** estão na mesma ordem como as entradas na estrutura de **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="1ca12-127">All of the entries in the **FLAGLIST** structure are in the same order as the entries in the **ADRLIST** structure.</span></span> <span data-ttu-id="1ca12-128">Isso facilita associar a um destinatário de uma configuração de sinalizador.</span><span class="sxs-lookup"><span data-stu-id="1ca12-128">This makes it easy to associate a flag setting with a recipient.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ca12-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ca12-129">See also</span></span>



[<span data-ttu-id="1ca12-130">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="1ca12-130">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="1ca12-131">IABContainer:: ResolveNames</span><span class="sxs-lookup"><span data-stu-id="1ca12-131">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="1ca12-132">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="1ca12-132">MAPI Structures</span></span>](mapi-structures.md)

