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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279706"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a><span data-ttu-id="36393-103">Propriedade canônica PidTagLastModificationTime</span><span class="sxs-lookup"><span data-stu-id="36393-103">PidTagLastModificationTime Canonical Property</span></span>

  
  
<span data-ttu-id="36393-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36393-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36393-105">Contém a data e a hora da última modificação do objeto ou subobjeto.</span><span class="sxs-lookup"><span data-stu-id="36393-105">Contains the date and time when the object or subobject was last modified.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36393-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="36393-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="36393-107">PR_LAST_MODIFICATION_TIME</span><span class="sxs-lookup"><span data-stu-id="36393-107">PR_LAST_MODIFICATION_TIME</span></span>  <br/> |
|<span data-ttu-id="36393-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="36393-108">Identifier:</span></span>  <br/> |<span data-ttu-id="36393-109">0x3008</span><span class="sxs-lookup"><span data-stu-id="36393-109">0x3008</span></span>  <br/> |
|<span data-ttu-id="36393-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="36393-110">Data type:</span></span>  <br/> |<span data-ttu-id="36393-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="36393-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="36393-112">Área:</span><span class="sxs-lookup"><span data-stu-id="36393-112">Area:</span></span>  <br/> |<span data-ttu-id="36393-113">Hora da mensagem</span><span class="sxs-lookup"><span data-stu-id="36393-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36393-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="36393-114">Remarks</span></span>

<span data-ttu-id="36393-115">Essa propriedade é definida inicialmente como o mesmo valor que a propriedade **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="36393-115">This property is initially set to the same value as the **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)) property.</span></span> <span data-ttu-id="36393-116">Os subobjetos de anexo podem atualizá-lo conforme necessário, copiando o horário da última modificação mantido pelo sistema de arquivos nativo.</span><span class="sxs-lookup"><span data-stu-id="36393-116">Attachment subobjects can update it as necessary by copying the last modification time maintained by the native file system.</span></span> <span data-ttu-id="36393-117">Um aplicativo cliente pode definir essa propriedade até a primeira chamada para o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="36393-117">A client application can set this property until the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="36393-118">De então no provedor deve atualizar o **PR_LAST_MODIFICATION_TIME** durante cada **IMAPIProp:: SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="36393-118">From then on the provider should update **PR_LAST_MODIFICATION_TIME** during every **IMAPIProp::SaveChanges** call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="36393-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="36393-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="36393-120">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="36393-120">Protocol specifications</span></span>

<span data-ttu-id="36393-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36393-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36393-122">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="36393-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="36393-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36393-123">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36393-124">Manipula a sincronização de dados do objeto Messaging entre um servidor e um cliente.</span><span class="sxs-lookup"><span data-stu-id="36393-124">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="36393-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36393-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36393-126">Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="36393-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="36393-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="36393-127">Header files</span></span>

<span data-ttu-id="36393-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="36393-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="36393-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="36393-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="36393-130">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="36393-130">Mapitags.h</span></span>
  
> <span data-ttu-id="36393-131">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="36393-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="36393-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="36393-132">See also</span></span>



[<span data-ttu-id="36393-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="36393-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="36393-134">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="36393-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="36393-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="36393-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="36393-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="36393-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

