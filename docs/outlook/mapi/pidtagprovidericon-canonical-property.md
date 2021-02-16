---
title: Propriedade canônica PidTagProviderIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderIcon
api_type:
- COM
ms.assetid: 59c84b1f-13b5-484b-b703-2fb9fcc6c7eb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425635"
---
# <a name="pidtagprovidericon-canonical-property"></a><span data-ttu-id="6bccd-103">Propriedade canônica PidTagProviderIcon</span><span class="sxs-lookup"><span data-stu-id="6bccd-103">PidTagProviderIcon Canonical Property</span></span>

  
  
<span data-ttu-id="6bccd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bccd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bccd-105">Contém uma cadeia de caracteres Unicode que especifica um ícone ou ícones personalizados a serem exibidos para um provedor MAPI na barra de status do Microsoft Office Outlook nos estados online e offline.</span><span class="sxs-lookup"><span data-stu-id="6bccd-105">Contains a Unicode string that specifies a custom icon or icons to be displayed for a MAPI provider in the Microsoft Office Outlook status bar in both online and offline states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6bccd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6bccd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6bccd-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span><span class="sxs-lookup"><span data-stu-id="6bccd-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span></span>  <br/> |
|<span data-ttu-id="6bccd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6bccd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6bccd-109">0x3417</span><span class="sxs-lookup"><span data-stu-id="6bccd-109">0x3417</span></span>  <br/> |
|<span data-ttu-id="6bccd-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6bccd-110">Data type:</span></span>  <br/> |<span data-ttu-id="6bccd-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6bccd-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6bccd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6bccd-112">Area:</span></span>  <br/> |<span data-ttu-id="6bccd-113">Armazenamento de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="6bccd-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6bccd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bccd-114">Remarks</span></span>

<span data-ttu-id="6bccd-115">Essas propriedades especificam o arquivo de recurso que contém um ícone personalizado que representa um provedor MAPI em um estado online e, opcionalmente, outro ícone personalizado no estado offline.</span><span class="sxs-lookup"><span data-stu-id="6bccd-115">These properties specify the resource file that contains a custom icon that represents a MAPI provider in an online state, and optionally, another custom icon in the offline state.</span></span> <span data-ttu-id="6bccd-116">O Outlook sempre solicita essas propriedades na representação Unicode.</span><span class="sxs-lookup"><span data-stu-id="6bccd-116">Outlook always requests these properties in Unicode representation.</span></span> 
  
<span data-ttu-id="6bccd-117">Por exemplo, o seguinte valor de propriedade instrui o Outlook a carregar a ID de ícone 1001 do módulo mymod32.dll e usar esse ícone para o estado online:  `mymod32.dll,#1001` .</span><span class="sxs-lookup"><span data-stu-id="6bccd-117">For example, the following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state:  `mymod32.dll,#1001`.</span></span> <span data-ttu-id="6bccd-118">Como não há nenhum ícone específico do provedor para o estado offline, nesse caso, o ícone offline padrão do Outlook é usado na barra de status.</span><span class="sxs-lookup"><span data-stu-id="6bccd-118">Since there is no provider-specific icon for the offline state, in this case, the standard Outlook offline icon is used in the status bar.</span></span> 
  
<span data-ttu-id="6bccd-119">O valor da propriedade a seguir instrui o Outlook a carregar a ID de ícone 1001 do módulo mymod32.dll e usar esse ícone para o estado online e também carregar a ID de ícone 1002 desse mesmo módulo a ser usado para o estado offline:  `mymod32.dll,#1001,#1002` .</span><span class="sxs-lookup"><span data-stu-id="6bccd-119">The following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state, and to also load icon ID 1002 from this same module to be used for the offline state:  `mymod32.dll,#1001,#1002`.</span></span> <span data-ttu-id="6bccd-120">Nenhum ícone do Outlook é usado na barra de status.</span><span class="sxs-lookup"><span data-stu-id="6bccd-120">No Outlook icon is used in the status bar.</span></span> 
  
<span data-ttu-id="6bccd-121">Por padrão, se nenhum ícone personalizado for especificado, o provedor será representado pelos ícones padrão do Outlook para o estado online e o estado offline.</span><span class="sxs-lookup"><span data-stu-id="6bccd-121">By default, if no custom icons are specified, the provider is represented by the Outlook default icons for the online state and the offline state.</span></span> <span data-ttu-id="6bccd-122">Opcionalmente, o provedor pode especificar um nome para exibição a ser exibido adjacente ao ícone na barra de status.</span><span class="sxs-lookup"><span data-stu-id="6bccd-122">The provider can optionally specify a display name to be shown adjacent to the icon in the status bar.</span></span> <span data-ttu-id="6bccd-123">Para obter mais informações, **consulte PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6bccd-123">For more information, see **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6bccd-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6bccd-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6bccd-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="6bccd-125">Header files</span></span>

<span data-ttu-id="6bccd-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6bccd-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6bccd-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6bccd-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="6bccd-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6bccd-128">Mapitags.h</span></span>
  
> <span data-ttu-id="6bccd-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6bccd-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6bccd-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bccd-130">See also</span></span>



[<span data-ttu-id="6bccd-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6bccd-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6bccd-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="6bccd-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6bccd-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6bccd-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6bccd-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6bccd-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

