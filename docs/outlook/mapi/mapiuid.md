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
ms.openlocfilehash: f7ec60768ab07c56969f538f196a1f9df5dbed17
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587163"
---
# <a name="mapiuid"></a><span data-ttu-id="85c10-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="85c10-103">MAPIUID</span></span>

  
  
<span data-ttu-id="85c10-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85c10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85c10-105">Uma versão independente da ordem de byte de uma estrutura [GUID](guid.md) é utilizada para identificar exclusivamente um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="85c10-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85c10-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="85c10-106">Header file:</span></span>  <br/> |<span data-ttu-id="85c10-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="85c10-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="85c10-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="85c10-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="85c10-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="85c10-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="85c10-110">Members</span><span class="sxs-lookup"><span data-stu-id="85c10-110">Members</span></span>

 <span data-ttu-id="85c10-111">**AB**</span><span class="sxs-lookup"><span data-stu-id="85c10-111">**ab**</span></span>
  
> <span data-ttu-id="85c10-112">Uma matriz que contém um identificador de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="85c10-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="85c10-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="85c10-113">Remarks</span></span>

<span data-ttu-id="85c10-114">Uma estrutura **MAPIUID** é uma estrutura **GUID** colocar em ordem de bytes de processador Intel®.</span><span class="sxs-lookup"><span data-stu-id="85c10-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="85c10-115">MAPI cria **MAPIUID** estruturas de forma que torna muito rara para dois itens diferentes ter o mesmo identificador.</span><span class="sxs-lookup"><span data-stu-id="85c10-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="85c10-116">Estruturas **MAPIUID** podem ser armazenadas como propriedades binárias ou como arquivos, sem relação com a ordem dos bytes do computador armazenando ou acessando as informações.</span><span class="sxs-lookup"><span data-stu-id="85c10-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="85c10-117">Estruturas **MAPIUID** são usadas:</span><span class="sxs-lookup"><span data-stu-id="85c10-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="85c10-118">Para identificar uma seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="85c10-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="85c10-119">Na entrada identificadores de mensagem armazenam em objetos de catálogo para identificar o provedor de serviços responsável de endereços.</span><span class="sxs-lookup"><span data-stu-id="85c10-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="85c10-120">Na propriedade **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) das mensagens.</span><span class="sxs-lookup"><span data-stu-id="85c10-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="85c10-121">Para gerar um identificador **MAPIUID** por uma chave de pesquisa, provedores de serviços de chamarem [IMAPISupport::NewUID](imapisupport-newuid.md).</span><span class="sxs-lookup"><span data-stu-id="85c10-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="85c10-122">Quando um cliente transmite uma mensagem em uma rede, ele deve usar um formato de transmissão ou protocolo que não alterar a ordem de bytes de dados **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="85c10-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="85c10-123">Para obter mais informações sobre como as estruturas **MAPIUID** são usadas, consulte os tópicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="85c10-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="85c10-124">Registrar identificadores exclusivos do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="85c10-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="85c10-125">Configurar um pedido de transporte</span><span class="sxs-lookup"><span data-stu-id="85c10-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="85c10-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="85c10-126">See also</span></span>



[<span data-ttu-id="85c10-127">GUID</span><span class="sxs-lookup"><span data-stu-id="85c10-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="85c10-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="85c10-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="85c10-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="85c10-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="85c10-130">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="85c10-130">MAPI Structures</span></span>](mapi-structures.md)

