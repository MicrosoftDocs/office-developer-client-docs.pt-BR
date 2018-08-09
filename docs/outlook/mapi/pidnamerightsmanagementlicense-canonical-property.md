---
title: Propriedade canônica PidNameRightsManagementLicense
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c75cb480b9a1a7ffdcff9c0f9b49aabba746fc3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768864"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="bb625-103">Propriedade canônica PidNameRightsManagementLicense</span><span class="sxs-lookup"><span data-stu-id="bb625-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="bb625-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb625-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bb625-105">Armazena em cache a licença de uso para a mensagem de email gerenciadas por direitos.</span><span class="sxs-lookup"><span data-stu-id="bb625-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb625-106">Nomes amigáveis:</span><span class="sxs-lookup"><span data-stu-id="bb625-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="bb625-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bb625-107">None</span></span>  <br/> |
|<span data-ttu-id="bb625-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="bb625-108">Property set:</span></span>  <br/> |<span data-ttu-id="bb625-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="bb625-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="bb625-110">Nome da propriedade:</span><span class="sxs-lookup"><span data-stu-id="bb625-110">Property name:</span></span>  <br/> |<span data-ttu-id="bb625-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="bb625-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="bb625-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bb625-112">Data type:</span></span>  <br/> |<span data-ttu-id="bb625-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="bb625-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="bb625-114">Área:</span><span class="sxs-lookup"><span data-stu-id="bb625-114">Area:</span></span>  <br/> |<span data-ttu-id="bb625-115">Mensagens seguras</span><span class="sxs-lookup"><span data-stu-id="bb625-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb625-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb625-116">Remarks</span></span>

<span data-ttu-id="bb625-117">Se a propriedade estiver presente em uma mensagem de email gerenciadas por direitos, o primeiro valor dessa propriedade binário vários deve conter a licença de uso compactado ZLIB (conforme especificado em [RFC1950]) para a mensagem de email gerenciadas por direitos.</span><span class="sxs-lookup"><span data-stu-id="bb625-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bb625-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb625-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb625-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="bb625-119">Protocol specifications</span></span>

<span data-ttu-id="bb625-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb625-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb625-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="bb625-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bb625-122">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb625-122">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb625-123">Especifica as propriedades das mensagens codificadas direitos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="bb625-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb625-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bb625-124">Header files</span></span>

<span data-ttu-id="bb625-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb625-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb625-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bb625-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb625-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb625-127">See also</span></span>



[<span data-ttu-id="bb625-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bb625-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb625-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="bb625-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb625-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bb625-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb625-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bb625-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

