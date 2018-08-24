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
ms.openlocfilehash: fd98044868bbec36ed14fcf90deb2990039244b8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573737"
---
# <a name="pidtagattachsize-canonical-property"></a><span data-ttu-id="0111c-103">Propriedade canônica PidTagAttachSize</span><span class="sxs-lookup"><span data-stu-id="0111c-103">PidTagAttachSize Canonical Property</span></span>

  
  
<span data-ttu-id="0111c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0111c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0111c-105">Contém a soma, em bytes, dos tamanhos de todas as propriedades em um anexo.</span><span class="sxs-lookup"><span data-stu-id="0111c-105">Contains the sum, in bytes, of the sizes of all properties on an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0111c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0111c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0111c-107">PR_ATTACH_SIZE</span><span class="sxs-lookup"><span data-stu-id="0111c-107">PR_ATTACH_SIZE</span></span>  <br/> |
|<span data-ttu-id="0111c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0111c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0111c-109">0x0E20</span><span class="sxs-lookup"><span data-stu-id="0111c-109">0x0E20</span></span>  <br/> |
|<span data-ttu-id="0111c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0111c-110">Data type:</span></span>  <br/> |<span data-ttu-id="0111c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0111c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0111c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0111c-112">Area:</span></span>  <br/> |<span data-ttu-id="0111c-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="0111c-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0111c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0111c-114">Remarks</span></span>

<span data-ttu-id="0111c-115">É recomendável que o anexo subobjetos exponham a propriedade **PR_ATTACH_SIZE** .</span><span class="sxs-lookup"><span data-stu-id="0111c-115">It is recommended that attachment subobjects expose the **PR_ATTACH_SIZE** property.</span></span> <span data-ttu-id="0111c-116">A soma contida no **PR_ATTACH_SIZE** inclui o tamanho da propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) ou **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0111c-116">The sum contained in **PR_ATTACH_SIZE** includes the size of the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> <span data-ttu-id="0111c-117">Apropriadamente, **PR_ATTACH_SIZE** é geralmente maior do que o conteúdo do anexo sozinho.</span><span class="sxs-lookup"><span data-stu-id="0111c-117">Accordingly, **PR_ATTACH_SIZE** is usually larger than the contents of the attachment alone.</span></span> 
  
<span data-ttu-id="0111c-118">Essa propriedade pode ser usada para verificar o tamanho aproximado do anexo antes de executar uma transferência remota pelo modem e para exibir os indicadores de progresso quando salvar o anexo em disco.</span><span class="sxs-lookup"><span data-stu-id="0111c-118">This property can be used to check the approximate size of the attachment before performing a remote transfer by modem and to display progress indicators when saving the attachment to disk.</span></span> <span data-ttu-id="0111c-119">É especialmente útil com os objetos OLE anexados.</span><span class="sxs-lookup"><span data-stu-id="0111c-119">It is particularly useful with attached OLE objects.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0111c-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0111c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0111c-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0111c-121">Protocol specifications</span></span>

<span data-ttu-id="0111c-122">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0111c-122">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0111c-123">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="0111c-123">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0111c-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0111c-124">Header files</span></span>

<span data-ttu-id="0111c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0111c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0111c-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0111c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0111c-127">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0111c-127">mapitags.h</span></span>
  
> <span data-ttu-id="0111c-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0111c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0111c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0111c-129">See also</span></span>



[<span data-ttu-id="0111c-130">Propriedade canônica PidTagMessageSize</span><span class="sxs-lookup"><span data-stu-id="0111c-130">PidTagMessageSize Canonical Property</span></span>](pidtagmessagesize-canonical-property.md)


[<span data-ttu-id="0111c-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0111c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0111c-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0111c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0111c-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0111c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0111c-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0111c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

