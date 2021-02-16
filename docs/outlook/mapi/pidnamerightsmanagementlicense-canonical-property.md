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
ms.openlocfilehash: 889b823a55c39ebc19e52c8cc9a1d078a5732a01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315019"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="3ba20-103">Propriedade canônica PidNameRightsManagementLicense</span><span class="sxs-lookup"><span data-stu-id="3ba20-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="3ba20-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ba20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ba20-105">Armazena em cache a licença de uso para a mensagem de email com direitos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="3ba20-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3ba20-106">Nomes amigáveis:</span><span class="sxs-lookup"><span data-stu-id="3ba20-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="3ba20-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3ba20-107">None</span></span>  <br/> |
|<span data-ttu-id="3ba20-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="3ba20-108">Property set:</span></span>  <br/> |<span data-ttu-id="3ba20-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="3ba20-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="3ba20-110">Nome da propriedade:</span><span class="sxs-lookup"><span data-stu-id="3ba20-110">Property name:</span></span>  <br/> |<span data-ttu-id="3ba20-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="3ba20-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="3ba20-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3ba20-112">Data type:</span></span>  <br/> |<span data-ttu-id="3ba20-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="3ba20-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="3ba20-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3ba20-114">Area:</span></span>  <br/> |<span data-ttu-id="3ba20-115">Mensagens seguras</span><span class="sxs-lookup"><span data-stu-id="3ba20-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ba20-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ba20-116">Remarks</span></span>

<span data-ttu-id="3ba20-117">Se a propriedade estiver presente em uma mensagem de email com direitos gerenciados, o primeiro valor dessa propriedade binária múltipla deverá conter a licença de uso compactada ZLIB (conforme especificado em [RFC1950]) para a mensagem de email gerenciada por direitos.</span><span class="sxs-lookup"><span data-stu-id="3ba20-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3ba20-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ba20-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3ba20-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3ba20-119">Protocol specifications</span></span>

<span data-ttu-id="3ba20-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ba20-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3ba20-121">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3ba20-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3ba20-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ba20-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3ba20-123">Especifica as propriedades de mensagens codificadas gerenciadas por direitos.</span><span class="sxs-lookup"><span data-stu-id="3ba20-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3ba20-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="3ba20-124">Header files</span></span>

<span data-ttu-id="3ba20-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3ba20-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="3ba20-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3ba20-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3ba20-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ba20-127">See also</span></span>



[<span data-ttu-id="3ba20-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3ba20-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3ba20-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3ba20-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3ba20-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3ba20-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3ba20-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3ba20-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

