---
title: Propriedade canônica PidTagDefaultViewEntryId Canonical
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6d284782de86b603e6bbe190931a85cd9196c88b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393513"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a><span data-ttu-id="cbc69-103">Propriedade canônica PidTagDefaultViewEntryId Canonical</span><span class="sxs-lookup"><span data-stu-id="cbc69-103">PidTagDefaultViewEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="cbc69-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbc69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbc69-105">Contém o identificador de entrada do modo de exibição da pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="cbc69-105">Contains the entry identifier of a folder's default view.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cbc69-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="cbc69-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cbc69-107">PR_DEFAULT_VIEW_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cbc69-107">PR_DEFAULT_VIEW_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="cbc69-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cbc69-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cbc69-109">0x3616</span><span class="sxs-lookup"><span data-stu-id="cbc69-109">0x3616</span></span>  <br/> |
|<span data-ttu-id="cbc69-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="cbc69-110">Data type:</span></span>  <br/> |<span data-ttu-id="cbc69-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cbc69-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cbc69-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cbc69-112">Area:</span></span>  <br/> |<span data-ttu-id="cbc69-113">Contêiner MAPI</span><span class="sxs-lookup"><span data-stu-id="cbc69-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbc69-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbc69-114">Remarks</span></span>

<span data-ttu-id="cbc69-115">Essa propriedade é o identificador de entrada da exibição da pasta que deve ser definido como o modo de exibição inicial.</span><span class="sxs-lookup"><span data-stu-id="cbc69-115">This property is the entry identifier of the folder view that should be set as the initial view.</span></span> <span data-ttu-id="cbc69-116">A propriedade não precisa ser definida se o modo de exibição do "Normal" deve ser usado como o modo de exibição inicial.</span><span class="sxs-lookup"><span data-stu-id="cbc69-116">The property need not be set if the "Normal" view is to be used as the initial view.</span></span>
  
<span data-ttu-id="cbc69-117">Um aplicativo cliente pode obter esta propriedade no momento em que ele abre a pasta e concretizar ganhos significativos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="cbc69-117">A client application can obtain this property at the time it opens the folder and realize significant performance gains.</span></span> <span data-ttu-id="cbc69-118">Esta propriedade pode ser usada como um atalho para obter o modo de exibição padrão, em vez de abrir a tabela de conteúdo associado e o envio de uma restrição.</span><span class="sxs-lookup"><span data-stu-id="cbc69-118">This property can be used as a shortcut to obtain the default view, instead of opening the associated contents table and submitting a restriction.</span></span>
  
<span data-ttu-id="cbc69-119">Uma implementação do provedor de serviço do método [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) pode copiar essa propriedade quando ele copia pastas.</span><span class="sxs-lookup"><span data-stu-id="cbc69-119">A service provider implementation of the [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) method can copy this property when it copies folders.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cbc69-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cbc69-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cbc69-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="cbc69-121">Protocol specifications</span></span>

<span data-ttu-id="cbc69-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbc69-122">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbc69-123">Trata as operações de pasta.</span><span class="sxs-lookup"><span data-stu-id="cbc69-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cbc69-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cbc69-124">Header files</span></span>

<span data-ttu-id="cbc69-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cbc69-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="cbc69-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="cbc69-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="cbc69-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cbc69-127">Mapitags.h</span></span>
  
> <span data-ttu-id="cbc69-128">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="cbc69-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cbc69-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbc69-129">See also</span></span>



[<span data-ttu-id="cbc69-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cbc69-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cbc69-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="cbc69-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cbc69-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="cbc69-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cbc69-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="cbc69-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

