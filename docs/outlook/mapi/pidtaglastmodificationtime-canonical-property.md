---
title: Propriedade canônica PidTagLastModificationTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dea709b457e28efef62718fc388621e01c4eb5bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387325"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a><span data-ttu-id="6820e-103">Propriedade canônica PidTagLastModificationTime</span><span class="sxs-lookup"><span data-stu-id="6820e-103">PidTagLastModificationTime Canonical Property</span></span>

  
  
<span data-ttu-id="6820e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6820e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6820e-105">Contém a data e hora que o objeto ou subobjeto última modificação.</span><span class="sxs-lookup"><span data-stu-id="6820e-105">Contains the date and time when the object or subobject was last modified.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6820e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6820e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6820e-107">PR_LAST_MODIFICATION_TIME</span><span class="sxs-lookup"><span data-stu-id="6820e-107">PR_LAST_MODIFICATION_TIME</span></span>  <br/> |
|<span data-ttu-id="6820e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6820e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6820e-109">0x3008</span><span class="sxs-lookup"><span data-stu-id="6820e-109">0x3008</span></span>  <br/> |
|<span data-ttu-id="6820e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6820e-110">Data type:</span></span>  <br/> |<span data-ttu-id="6820e-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="6820e-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="6820e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6820e-112">Area:</span></span>  <br/> |<span data-ttu-id="6820e-113">Hora da mensagem</span><span class="sxs-lookup"><span data-stu-id="6820e-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6820e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6820e-114">Remarks</span></span>

<span data-ttu-id="6820e-115">Essa propriedade é definida inicialmente para o mesmo valor que a propriedade **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6820e-115">This property is initially set to the same value as the **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) property.</span></span> <span data-ttu-id="6820e-116">Anexo subobjetos atualizá-la, conforme necessário, copiando a hora da última modificação mantida pelo sistema de arquivo nativo.</span><span class="sxs-lookup"><span data-stu-id="6820e-116">Attachment subobjects can update it as necessary by copying the last modification time maintained by the native file system.</span></span> <span data-ttu-id="6820e-117">Um aplicativo cliente pode definir essa propriedade até a primeira chamada ao método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="6820e-117">A client application can set this property until the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="6820e-118">A partir do provedor deve atualizar **PR_LAST_MODIFICATION_TIME** durante cada chamada **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="6820e-118">From then on the provider should update **PR_LAST_MODIFICATION_TIME** during every **IMAPIProp::SaveChanges** call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6820e-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6820e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6820e-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6820e-120">Protocol specifications</span></span>

<span data-ttu-id="6820e-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6820e-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6820e-122">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="6820e-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6820e-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6820e-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6820e-124">Trata-se de sincronização de dados de objeto de mensagens entre um servidor e um cliente.</span><span class="sxs-lookup"><span data-stu-id="6820e-124">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="6820e-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6820e-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6820e-126">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="6820e-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6820e-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6820e-127">Header files</span></span>

<span data-ttu-id="6820e-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6820e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="6820e-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6820e-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="6820e-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6820e-130">Mapitags.h</span></span>
  
> <span data-ttu-id="6820e-131">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6820e-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6820e-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="6820e-132">See also</span></span>



[<span data-ttu-id="6820e-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6820e-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6820e-134">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6820e-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6820e-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6820e-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6820e-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6820e-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

