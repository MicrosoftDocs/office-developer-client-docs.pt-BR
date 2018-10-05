---
title: Propriedade canônica PidTagItemTemporaryflags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagItemTemporaryflags
api_type:
- HeaderDef
ms.assetid: 8066de8e-2b77-4bac-8df3-e64b03ee42b9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ec092e6cc6174e156dbfe7784143c9d74715eef7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392967"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a><span data-ttu-id="c0ae2-103">Propriedade canônica PidTagItemTemporaryflags</span><span class="sxs-lookup"><span data-stu-id="c0ae2-103">PidTagItemTemporaryflags Canonical Property</span></span>

  
  
<span data-ttu-id="c0ae2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0ae2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0ae2-105">Contém um sinalizador que indica que uma mensagem foi lida, mas não está marcada como lidos.</span><span class="sxs-lookup"><span data-stu-id="c0ae2-105">Contains a flag that indicates that a message has been read, but not marked as read.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0ae2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c0ae2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c0ae2-107">PR_ITEM_TMPFLAGS</span><span class="sxs-lookup"><span data-stu-id="c0ae2-107">PR_ITEM_TMPFLAGS</span></span>  <br/> |
|<span data-ttu-id="c0ae2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c0ae2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c0ae2-109">0x1097</span><span class="sxs-lookup"><span data-stu-id="c0ae2-109">0x1097</span></span>  <br/> |
|<span data-ttu-id="c0ae2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c0ae2-110">Data type:</span></span>  <br/> |<span data-ttu-id="c0ae2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c0ae2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c0ae2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c0ae2-112">Area:</span></span>  <br/> |<span data-ttu-id="c0ae2-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="c0ae2-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0ae2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0ae2-114">Remarks</span></span>

<span data-ttu-id="c0ae2-115">Essa propriedade é usada na pasta de pesquisa de mensagens não lidas do Outlook para controlar as mensagens que tenham sido lidas sem realmente marcá-las como lidos, qual remover da pasta.</span><span class="sxs-lookup"><span data-stu-id="c0ae2-115">This property is used in Outlook's Unread Messages search folder to keep track of which messages have been read without actually marking them as read, which would remove them from the folder.</span></span> <span data-ttu-id="c0ae2-116">Quando as alterações de modo de exibição, essa propriedade é removida e o item está marcado como lidos.</span><span class="sxs-lookup"><span data-stu-id="c0ae2-116">When the view changes this property is removed and the item is marked as read.</span></span> <span data-ttu-id="c0ae2-117">Essa propriedade não será sincronizado com o servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="c0ae2-117">This property will not synchronize to the Exchange Server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c0ae2-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0ae2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c0ae2-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="c0ae2-119">Protocol specifications</span></span>

<span data-ttu-id="c0ae2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0ae2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0ae2-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c0ae2-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c0ae2-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0ae2-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0ae2-123">Trata as operações de pasta.</span><span class="sxs-lookup"><span data-stu-id="c0ae2-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c0ae2-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c0ae2-124">Header files</span></span>

<span data-ttu-id="c0ae2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0ae2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c0ae2-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c0ae2-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c0ae2-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c0ae2-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c0ae2-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c0ae2-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0ae2-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0ae2-129">See also</span></span>



[<span data-ttu-id="c0ae2-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c0ae2-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c0ae2-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c0ae2-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c0ae2-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c0ae2-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c0ae2-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c0ae2-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

