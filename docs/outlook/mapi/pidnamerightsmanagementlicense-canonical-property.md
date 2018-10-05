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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395541"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a><span data-ttu-id="0fdc2-103">Propriedade canônica PidNameRightsManagementLicense</span><span class="sxs-lookup"><span data-stu-id="0fdc2-103">PidNameRightsManagementLicense Canonical Property</span></span>

  
  
<span data-ttu-id="0fdc2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fdc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fdc2-105">Armazena em cache a licença de uso para a mensagem de email gerenciadas por direitos.</span><span class="sxs-lookup"><span data-stu-id="0fdc2-105">Caches the use license for the rights-managed email message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0fdc2-106">Nomes amigáveis:</span><span class="sxs-lookup"><span data-stu-id="0fdc2-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="0fdc2-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0fdc2-107">None</span></span>  <br/> |
|<span data-ttu-id="0fdc2-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="0fdc2-108">Property set:</span></span>  <br/> |<span data-ttu-id="0fdc2-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="0fdc2-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="0fdc2-110">Nome da propriedade:</span><span class="sxs-lookup"><span data-stu-id="0fdc2-110">Property name:</span></span>  <br/> |<span data-ttu-id="0fdc2-111">DRMLicense</span><span class="sxs-lookup"><span data-stu-id="0fdc2-111">DRMLicense</span></span>  <br/> |
|<span data-ttu-id="0fdc2-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0fdc2-112">Data type:</span></span>  <br/> |<span data-ttu-id="0fdc2-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="0fdc2-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="0fdc2-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0fdc2-114">Area:</span></span>  <br/> |<span data-ttu-id="0fdc2-115">Mensagens seguras</span><span class="sxs-lookup"><span data-stu-id="0fdc2-115">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0fdc2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fdc2-116">Remarks</span></span>

<span data-ttu-id="0fdc2-117">Se a propriedade estiver presente em uma mensagem de email gerenciadas por direitos, o primeiro valor dessa propriedade binário vários deve conter a licença de uso compactado ZLIB (conforme especificado em [RFC1950]) para a mensagem de email gerenciadas por direitos.</span><span class="sxs-lookup"><span data-stu-id="0fdc2-117">If the property is present on a rights-managed email message, the first value of this multiple binary property must contain the ZLIB (as specified in [RFC1950]) compressed use license for the rights-managed email message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0fdc2-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0fdc2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0fdc2-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0fdc2-119">Protocol specifications</span></span>

<span data-ttu-id="0fdc2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fdc2-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fdc2-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0fdc2-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0fdc2-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fdc2-122">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fdc2-123">Especifica as propriedades das mensagens codificadas direitos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="0fdc2-123">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0fdc2-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0fdc2-124">Header files</span></span>

<span data-ttu-id="0fdc2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0fdc2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0fdc2-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0fdc2-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0fdc2-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fdc2-127">See also</span></span>



[<span data-ttu-id="0fdc2-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0fdc2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0fdc2-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0fdc2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0fdc2-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0fdc2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0fdc2-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0fdc2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

