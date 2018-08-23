---
title: Propriedade canônica PidLidSpamOriginalFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSpamOriginalFolder
api_type:
- COM
ms.assetid: 45846fe3-7ab3-4019-98bb-fe615889c31c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 639d5e96eb56fb543d6a6026b1c9400631cee819
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593337"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a><span data-ttu-id="35e3c-103">Propriedade canônica PidLidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="35e3c-103">PidLidSpamOriginalFolder Canonical Property</span></span>

  
  
<span data-ttu-id="35e3c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35e3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35e3c-105">Indica a pasta na qual uma mensagem se encontrava antes que ele foi filtrada para a pasta Lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="35e3c-105">Indicates which folder a message was in before it was filtered into the junk email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35e3c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="35e3c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="35e3c-107">dispidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="35e3c-107">dispidSpamOriginalFolder</span></span>  <br/> |
|<span data-ttu-id="35e3c-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="35e3c-108">Property set:</span></span>  <br/> |<span data-ttu-id="35e3c-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="35e3c-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="35e3c-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="35e3c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="35e3c-111">0x0000859C</span><span class="sxs-lookup"><span data-stu-id="35e3c-111">0x0000859C</span></span>  <br/> |
|<span data-ttu-id="35e3c-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="35e3c-112">Data type:</span></span>  <br/> |<span data-ttu-id="35e3c-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="35e3c-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="35e3c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="35e3c-114">Area:</span></span>  <br/> |<span data-ttu-id="35e3c-115">Spam</span><span class="sxs-lookup"><span data-stu-id="35e3c-115">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35e3c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="35e3c-116">Remarks</span></span>

<span data-ttu-id="35e3c-117">O valor dessa propriedade é a **EntryID** da pasta que continha a mensagem antes de ser movida.</span><span class="sxs-lookup"><span data-stu-id="35e3c-117">The value of this property is the **EntryID** of the folder that contained the message before it was moved.</span></span> <span data-ttu-id="35e3c-118">Essa propriedade deve ser definida quando uma mensagem é marcada como spam.</span><span class="sxs-lookup"><span data-stu-id="35e3c-118">This property should be set when a message is marked as spam.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="35e3c-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="35e3c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="35e3c-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="35e3c-120">Protocol specifications</span></span>

<span data-ttu-id="35e3c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35e3c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35e3c-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="35e3c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="35e3c-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="35e3c-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="35e3c-124">Permite a manipulação das listas de permitir/bloquear e a determinação das mensagens de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="35e3c-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="35e3c-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="35e3c-125">Header files</span></span>

<span data-ttu-id="35e3c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35e3c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="35e3c-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="35e3c-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35e3c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="35e3c-128">See also</span></span>



[<span data-ttu-id="35e3c-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="35e3c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="35e3c-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="35e3c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="35e3c-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="35e3c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="35e3c-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="35e3c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

