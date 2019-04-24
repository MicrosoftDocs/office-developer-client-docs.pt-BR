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
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="a2373-103">Propriedade canônica PidNameRightsManagementLicense</span><span class="sxs-lookup"><span data-stu-id="a2373-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="a2373-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2373-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2373-105">Armazena em cache a licença de uso da mensagem de email gerenciada por direitos.</span><span class="sxs-lookup"><span data-stu-id="a2373-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a2373-106">Nomes amigáveis:</span><span class="sxs-lookup"><span data-stu-id="a2373-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="a2373-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a2373-107">None</span></span>  <br/> |
|<span data-ttu-id="a2373-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="a2373-108">Property set:</span></span>  <br/> |<span data-ttu-id="a2373-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="a2373-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="a2373-110">Nome da propriedade:</span><span class="sxs-lookup"><span data-stu-id="a2373-110">Property name:</span></span>  <br/> |<span data-ttu-id="a2373-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="a2373-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="a2373-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a2373-112">Data type:</span></span>  <br/> |<span data-ttu-id="a2373-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="a2373-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="a2373-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a2373-114">Area:</span></span>  <br/> |<span data-ttu-id="a2373-115">Mensagens seguras</span><span class="sxs-lookup"><span data-stu-id="a2373-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2373-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2373-116">Remarks</span></span>

<span data-ttu-id="a2373-117">Se a propriedade estiver presente em uma mensagem de email gerenciada por direitos, o primeiro valor dessa propriedade Binary Multiple deverá conter o ZLIB (conforme especificado em [RFC1950]) licença de uso compactada para a mensagem de email gerenciada por direitos.</span><span class="sxs-lookup"><span data-stu-id="a2373-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a2373-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2373-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a2373-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="a2373-119">Protocol specifications</span></span>

<span data-ttu-id="a2373-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2373-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2373-121">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a2373-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a2373-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2373-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2373-123">Especifica as propriedades de mensagens codificadas por direitos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="a2373-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a2373-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a2373-124">Header files</span></span>

<span data-ttu-id="a2373-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a2373-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a2373-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a2373-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a2373-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2373-127">See also</span></span>



[<span data-ttu-id="a2373-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a2373-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a2373-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a2373-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a2373-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a2373-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a2373-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a2373-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

