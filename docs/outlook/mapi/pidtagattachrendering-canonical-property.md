---
title: Propriedade canônica PidTagAttachRendering
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachRendering
api_type:
- HeaderDef
ms.assetid: 1f31f7f4-fbda-4337-95e5-5474dd1bf84a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 22d3e649641dbe688912ecece7fde73a555f4a88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361093"
---
# <a name="pidtagattachrendering-canonical-property"></a><span data-ttu-id="2cec2-103">Propriedade canônica PidTagAttachRendering</span><span class="sxs-lookup"><span data-stu-id="2cec2-103">PidTagAttachRendering Canonical Property</span></span>

  
  
<span data-ttu-id="2cec2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2cec2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2cec2-105">Contém um metarquivo do Microsoft Windows com informações de renderização de um anexo.</span><span class="sxs-lookup"><span data-stu-id="2cec2-105">Contains a Microsoft Windows metafile with rendering information for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2cec2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2cec2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2cec2-107">PR_ATTACH_RENDERING</span><span class="sxs-lookup"><span data-stu-id="2cec2-107">PR_ATTACH_RENDERING</span></span>  <br/> |
|<span data-ttu-id="2cec2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2cec2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2cec2-109">0x3709</span><span class="sxs-lookup"><span data-stu-id="2cec2-109">0x3709</span></span>  <br/> |
|<span data-ttu-id="2cec2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2cec2-110">Data type:</span></span>  <br/> |<span data-ttu-id="2cec2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2cec2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2cec2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2cec2-112">Area:</span></span>  <br/> |<span data-ttu-id="2cec2-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="2cec2-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2cec2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2cec2-114">Remarks</span></span>

<span data-ttu-id="2cec2-115">A finalidade dessa propriedade é fornecer um ícone ou outra representação de ilustrações que possa ser exibida dentro da mensagem pai no ponto de anexo.</span><span class="sxs-lookup"><span data-stu-id="2cec2-115">The purpose of this property is to provide an icon or other pictorial representation that can be displayed within the parent message at the point of attachment.</span></span> <span data-ttu-id="2cec2-116">Essa representação normalmente inclui o nome do anexo, se houver, e a natureza do anexo, como um documento do Microsoft Office Word.</span><span class="sxs-lookup"><span data-stu-id="2cec2-116">Such representation typically includes the name of the attachment, if any, and the nature of the attachment, such as a Microsoft Office Word document.</span></span> <span data-ttu-id="2cec2-117">Um aplicativo cliente pode usar essa representação na exibição da mensagem.</span><span class="sxs-lookup"><span data-stu-id="2cec2-117">A client application can use this representation in the display of the message.</span></span> 
  
<span data-ttu-id="2cec2-118">Para um arquivo anexado, essa propriedade normalmente retrata um ícone para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="2cec2-118">For an attached file, this property usually portrays an icon for the file.</span></span> 
  
<span data-ttu-id="2cec2-119">Para uma mensagem anexada, esta propriedade normalmente não é definida.</span><span class="sxs-lookup"><span data-stu-id="2cec2-119">For an attached message, this property is typically not set.</span></span> <span data-ttu-id="2cec2-120">Um aplicativo cliente que precisa processar uma mensagem anexada deve obter sua propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), chamar [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para um ponteiro para o objeto de informações de formulário correspondente Abra a interface [IMAPIFormInfo](imapiforminfoimapiprop.md) nesse objeto e use GetProps para recuperar a propriedade **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2cec2-120">A client application needing to render an attached message should obtain its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) for a pointer to the corresponding form information object, open the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface on that object, and use **GetProps** to retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="2cec2-121">Para um objeto OLE estático incorporado, esta propriedade contém um metarquivo do Microsoft Windows que pode ser usado para desenhar a representação de anexo em uma janela.</span><span class="sxs-lookup"><span data-stu-id="2cec2-121">For an embedded static OLE object, this property contains a Microsoft Windows metafile that can be used to draw the attachment representation in a window.</span></span> 
  
<span data-ttu-id="2cec2-122">Para um objeto OLE dinâmico incorporado, o cliente deve usar os dados OLE para gerar as informações de renderização.</span><span class="sxs-lookup"><span data-stu-id="2cec2-122">For an embedded dynamic OLE object, the client should use the OLE data to generate the rendering information.</span></span> 
  
<span data-ttu-id="2cec2-123">Em todos os casos, o aplicativo cliente deve estar ciente de que essa propriedade normalmente é de várias centenas de bytes de tamanho e está sujeita a truncamento na tabela de anexos.</span><span class="sxs-lookup"><span data-stu-id="2cec2-123">In all cases, the client application should be aware that this property is usually several hundred bytes in size and is subject to truncation in the attachment table.</span></span> <span data-ttu-id="2cec2-124">Se um cliente quiser renderizar o anexo dessa propriedade sem abrir o próprio anexo, ele deverá funcionar dentro da regra de truncamento da tabela.</span><span class="sxs-lookup"><span data-stu-id="2cec2-124">If a client wishes to render the attachment from this property without opening the attachment itself, it must work within the table truncation rule.</span></span> <span data-ttu-id="2cec2-125">Para obter mais informações, consulte [trabalhar com colunas grandes](working-with-large-columns.md).</span><span class="sxs-lookup"><span data-stu-id="2cec2-125">For more information, see [Working with Large Columns](working-with-large-columns.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2cec2-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2cec2-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2cec2-127">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="2cec2-127">Protocol specifications</span></span>

<span data-ttu-id="2cec2-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2cec2-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2cec2-129">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="2cec2-129">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2cec2-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2cec2-130">Header files</span></span>

<span data-ttu-id="2cec2-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2cec2-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="2cec2-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2cec2-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="2cec2-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2cec2-133">Mapitags.h</span></span>
  
> <span data-ttu-id="2cec2-134">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="2cec2-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2cec2-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="2cec2-135">See also</span></span>



[<span data-ttu-id="2cec2-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2cec2-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2cec2-137">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2cec2-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2cec2-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2cec2-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2cec2-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2cec2-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

