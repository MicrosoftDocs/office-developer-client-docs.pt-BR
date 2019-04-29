---
title: Propriedade canônica PidTagOwnStoreEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnStoreEntryId
api_type:
- COM
ms.assetid: 6a82ee90-10a1-49e0-8f3a-a2cd9f490f99
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 16a23c4e711bf9f7b670dff8b3e8f65371aa6bda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427371"
---
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="abbee-103">Propriedade canônica PidTagOwnStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="abbee-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="abbee-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abbee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abbee-105">Contém o identificador de entrada de um repositório de mensagens rigidamente acoplado de um transporte.</span><span class="sxs-lookup"><span data-stu-id="abbee-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="abbee-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="abbee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="abbee-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="abbee-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="abbee-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="abbee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="abbee-109">0x3E06</span><span class="sxs-lookup"><span data-stu-id="abbee-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="abbee-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="abbee-110">Data type:</span></span>  <br/> |<span data-ttu-id="abbee-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="abbee-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="abbee-112">Área:</span><span class="sxs-lookup"><span data-stu-id="abbee-112">Area:</span></span>  <br/> |<span data-ttu-id="abbee-113">Propriedades do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="abbee-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abbee-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="abbee-114">Remarks</span></span>

<span data-ttu-id="abbee-115">Esta propriedade especifica o identificador de entrada para o repositório rigidamente acoplado, se houver um.</span><span class="sxs-lookup"><span data-stu-id="abbee-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="abbee-116">Por exemplo, um provedor de transporte pode especificar o identificador de entrada de armazenamento de pasta particular para que o spooler MAPI possa conectar o provedor de transporte ao repositório.</span><span class="sxs-lookup"><span data-stu-id="abbee-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="abbee-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="abbee-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="abbee-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="abbee-118">Header files</span></span>

<span data-ttu-id="abbee-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="abbee-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="abbee-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="abbee-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="abbee-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="abbee-121">Mapitags.h</span></span>
  
> <span data-ttu-id="abbee-122">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="abbee-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="abbee-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="abbee-123">See also</span></span>



[<span data-ttu-id="abbee-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="abbee-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="abbee-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="abbee-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="abbee-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="abbee-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="abbee-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="abbee-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

