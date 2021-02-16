---
title: Propriedade canônica PidTagAttachSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachSize
api_type:
- HeaderDef
ms.assetid: 768b3215-dd9f-4aa0-b52c-178ca81a7b07
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f3e4f19ab43a3da7c4840d762d5131813c83d996
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361086"
---
# <a name="pidtagattachsize-canonical-property"></a><span data-ttu-id="8d65f-103">Propriedade canônica PidTagAttachSize</span><span class="sxs-lookup"><span data-stu-id="8d65f-103">PidTagAttachSize Canonical Property</span></span>

  
  
<span data-ttu-id="8d65f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d65f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d65f-105">Contém a soma, em bytes, dos tamanhos de todas as propriedades em um anexo.</span><span class="sxs-lookup"><span data-stu-id="8d65f-105">Contains the sum, in bytes, of the sizes of all properties on an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d65f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8d65f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d65f-107">PR_ATTACH_SIZE</span><span class="sxs-lookup"><span data-stu-id="8d65f-107">PR_ATTACH_SIZE</span></span>  <br/> |
|<span data-ttu-id="8d65f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8d65f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d65f-109">0x0E20</span><span class="sxs-lookup"><span data-stu-id="8d65f-109">0x0E20</span></span>  <br/> |
|<span data-ttu-id="8d65f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8d65f-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d65f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8d65f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8d65f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8d65f-112">Area:</span></span>  <br/> |<span data-ttu-id="8d65f-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="8d65f-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d65f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d65f-114">Remarks</span></span>

<span data-ttu-id="8d65f-115">É recomendável que os subobjetos de anexo exponham **a PR_ATTACH_SIZE** propriedade.</span><span class="sxs-lookup"><span data-stu-id="8d65f-115">It is recommended that attachment subobjects expose the **PR_ATTACH_SIZE** property.</span></span> <span data-ttu-id="8d65f-116">A soma contida **no PR_ATTACH_SIZE** inclui o tamanho da propriedade **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8d65f-116">The sum contained in **PR_ATTACH_SIZE** includes the size of the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> <span data-ttu-id="8d65f-117">Da mesma forma, **PR_ATTACH_SIZE** geralmente é maior do que o conteúdo do anexo sozinho.</span><span class="sxs-lookup"><span data-stu-id="8d65f-117">Accordingly, **PR_ATTACH_SIZE** is usually larger than the contents of the attachment alone.</span></span> 
  
<span data-ttu-id="8d65f-118">Essa propriedade pode ser usada para verificar o tamanho aproximado do anexo antes de executar uma transferência remota pelo modem e para exibir indicadores de progresso ao salvar o anexo no disco.</span><span class="sxs-lookup"><span data-stu-id="8d65f-118">This property can be used to check the approximate size of the attachment before performing a remote transfer by modem and to display progress indicators when saving the attachment to disk.</span></span> <span data-ttu-id="8d65f-119">Ele é particularmente útil com objetos OLE anexados.</span><span class="sxs-lookup"><span data-stu-id="8d65f-119">It is particularly useful with attached OLE objects.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8d65f-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8d65f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d65f-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8d65f-121">Protocol specifications</span></span>

<span data-ttu-id="8d65f-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d65f-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d65f-123">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="8d65f-123">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d65f-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="8d65f-124">Header files</span></span>

<span data-ttu-id="8d65f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d65f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d65f-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8d65f-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d65f-127">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8d65f-127">mapitags.h</span></span>
  
> <span data-ttu-id="8d65f-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="8d65f-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d65f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d65f-129">See also</span></span>



[<span data-ttu-id="8d65f-130">Propriedade canônica PidTagMessageSize</span><span class="sxs-lookup"><span data-stu-id="8d65f-130">PidTagMessageSize Canonical Property</span></span>](pidtagmessagesize-canonical-property.md)


[<span data-ttu-id="8d65f-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8d65f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d65f-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8d65f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d65f-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8d65f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d65f-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8d65f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

