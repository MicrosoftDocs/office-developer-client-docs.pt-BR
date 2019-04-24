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
# <a name="pidtagattachsize-canonical-property"></a><span data-ttu-id="5febc-103">Propriedade canônica PidTagAttachSize</span><span class="sxs-lookup"><span data-stu-id="5febc-103">PidTagAttachSize Canonical Property</span></span>

  
  
<span data-ttu-id="5febc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5febc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5febc-105">Contém a soma, em bytes, dos tamanhos de todas as propriedades de um anexo.</span><span class="sxs-lookup"><span data-stu-id="5febc-105">Contains the sum, in bytes, of the sizes of all properties on an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5febc-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5febc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5febc-107">PR_ATTACH_SIZE</span><span class="sxs-lookup"><span data-stu-id="5febc-107">PR_ATTACH_SIZE</span></span>  <br/> |
|<span data-ttu-id="5febc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5febc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5febc-109">0x0E20</span><span class="sxs-lookup"><span data-stu-id="5febc-109">0x0E20</span></span>  <br/> |
|<span data-ttu-id="5febc-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5febc-110">Data type:</span></span>  <br/> |<span data-ttu-id="5febc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5febc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5febc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5febc-112">Area:</span></span>  <br/> |<span data-ttu-id="5febc-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="5febc-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5febc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5febc-114">Remarks</span></span>

<span data-ttu-id="5febc-115">É recomendável que os subobjetos de anexo exponham a propriedade **PR_ATTACH_SIZE** .</span><span class="sxs-lookup"><span data-stu-id="5febc-115">It is recommended that attachment subobjects expose the **PR_ATTACH_SIZE** property.</span></span> <span data-ttu-id="5febc-116">A soma contida no **PR_ATTACH_SIZE** inclui o tamanho da propriedade **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5febc-116">The sum contained in **PR_ATTACH_SIZE** includes the size of the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> <span data-ttu-id="5febc-117">Da mesma forma, **PR_ATTACH_SIZE** geralmente é maior do que o conteúdo do anexo.</span><span class="sxs-lookup"><span data-stu-id="5febc-117">Accordingly, **PR_ATTACH_SIZE** is usually larger than the contents of the attachment alone.</span></span> 
  
<span data-ttu-id="5febc-118">Essa propriedade pode ser usada para verificar o tamanho aproximado do anexo antes de executar uma transferência remota por modem e para exibir os indicadores de progresso ao salvar o anexo no disco.</span><span class="sxs-lookup"><span data-stu-id="5febc-118">This property can be used to check the approximate size of the attachment before performing a remote transfer by modem and to display progress indicators when saving the attachment to disk.</span></span> <span data-ttu-id="5febc-119">É particularmente útil com objetos OLE anexados.</span><span class="sxs-lookup"><span data-stu-id="5febc-119">It is particularly useful with attached OLE objects.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5febc-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5febc-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5febc-121">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="5febc-121">Protocol specifications</span></span>

<span data-ttu-id="5febc-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5febc-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5febc-123">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="5febc-123">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5febc-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5febc-124">Header files</span></span>

<span data-ttu-id="5febc-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5febc-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5febc-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5febc-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="5febc-127">mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5febc-127">mapitags.h</span></span>
  
> <span data-ttu-id="5febc-128">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="5febc-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5febc-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5febc-129">See also</span></span>



[<span data-ttu-id="5febc-130">Propriedade canônica PidTagMessageSize</span><span class="sxs-lookup"><span data-stu-id="5febc-130">PidTagMessageSize Canonical Property</span></span>](pidtagmessagesize-canonical-property.md)


[<span data-ttu-id="5febc-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5febc-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5febc-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="5febc-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5febc-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5febc-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5febc-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5febc-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

