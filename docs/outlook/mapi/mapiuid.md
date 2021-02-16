---
title: MAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da314205f7d2dd746b72aa7e2b5ff2a13bb0c21b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432202"
---
# <a name="mapiuid"></a><span data-ttu-id="cd287-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="cd287-103">MAPIUID</span></span>

  
  
<span data-ttu-id="cd287-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd287-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd287-105">Uma versão independente de ordem de byte de uma estrutura [GUID](guid.md) usada para identificar exclusivamente um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="cd287-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd287-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="cd287-106">Header file:</span></span>  <br/> |<span data-ttu-id="cd287-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd287-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="cd287-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="cd287-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="cd287-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="cd287-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="cd287-110">Members</span><span class="sxs-lookup"><span data-stu-id="cd287-110">Members</span></span>

 <span data-ttu-id="cd287-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="cd287-111">**ab**</span></span>
  
> <span data-ttu-id="cd287-112">Uma matriz que contém um identificador de 16 byte.</span><span class="sxs-lookup"><span data-stu-id="cd287-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cd287-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd287-113">Remarks</span></span>

<span data-ttu-id="cd287-114">Uma **estrutura MAPIUID** é uma estrutura **GUID** colocada na ordem ® byte do processador Intel.</span><span class="sxs-lookup"><span data-stu-id="cd287-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="cd287-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span><span class="sxs-lookup"><span data-stu-id="cd287-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="cd287-116">**As estruturas MAPIUID** podem ser armazenadas como propriedades binárias ou como arquivos, sem considerar a ordenação de byte do computador que armazena ou acessa as informações.</span><span class="sxs-lookup"><span data-stu-id="cd287-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="cd287-117">**As estruturas MAPIUID** são usadas:</span><span class="sxs-lookup"><span data-stu-id="cd287-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="cd287-118">Para identificar uma seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="cd287-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="cd287-119">Nos identificadores de entrada do armazenamento de mensagens e dos objetos do livro de endereços para identificar o provedor de serviços responsável.</span><span class="sxs-lookup"><span data-stu-id="cd287-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="cd287-120">Na **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) das mensagens.</span><span class="sxs-lookup"><span data-stu-id="cd287-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="cd287-121">Para gerar um **identificador MAPIUID** para uma chave de pesquisa, os provedores de serviços chamam [IMAPISupport::NewUID](imapisupport-newuid.md).</span><span class="sxs-lookup"><span data-stu-id="cd287-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="cd287-122">Quando um cliente transmite uma mensagem através de uma rede, ele deve usar um protocolo ou formato de transmissão que não altere a ordem de byte dos dados **MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="cd287-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="cd287-123">Para obter mais informações sobre como as **estruturas MAPIUID** são usadas, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="cd287-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="cd287-124">Registrando identificadores exclusivos do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="cd287-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="cd287-125">Configurando a ordem de transporte</span><span class="sxs-lookup"><span data-stu-id="cd287-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="cd287-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd287-126">See also</span></span>



[<span data-ttu-id="cd287-127">GUID</span><span class="sxs-lookup"><span data-stu-id="cd287-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="cd287-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="cd287-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="cd287-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="cd287-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="cd287-130">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="cd287-130">MAPI Structures</span></span>](mapi-structures.md)

