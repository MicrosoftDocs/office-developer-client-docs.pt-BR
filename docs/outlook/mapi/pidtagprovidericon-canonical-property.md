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
ms.openlocfilehash: 61dc61872e8d1ed525d5ac3c46c56ccc3e45ea5e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593694"
---
# <a name="pidtagprovidericon-canonical-property"></a><span data-ttu-id="c15ce-103">Propriedade canônica PidTagProviderIcon</span><span class="sxs-lookup"><span data-stu-id="c15ce-103">PidTagProviderIcon Canonical Property</span></span>

  
  
<span data-ttu-id="c15ce-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c15ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c15ce-105">Contém uma cadeia de caracteres Unicode que especifica um ícone personalizado ou ícones a serem exibidos para um provedor MAPI na barra de status do Microsoft Office Outlook nos estados online e offline.</span><span class="sxs-lookup"><span data-stu-id="c15ce-105">Contains a Unicode string that specifies a custom icon or icons to be displayed for a MAPI provider in the Microsoft Office Outlook status bar in both online and offline states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c15ce-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c15ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c15ce-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span><span class="sxs-lookup"><span data-stu-id="c15ce-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span></span>  <br/> |
|<span data-ttu-id="c15ce-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c15ce-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c15ce-109">0x3417</span><span class="sxs-lookup"><span data-stu-id="c15ce-109">0x3417</span></span>  <br/> |
|<span data-ttu-id="c15ce-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c15ce-110">Data type:</span></span>  <br/> |<span data-ttu-id="c15ce-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c15ce-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c15ce-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c15ce-112">Area:</span></span>  <br/> |<span data-ttu-id="c15ce-113">Armazenamento de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="c15ce-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c15ce-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c15ce-114">Remarks</span></span>

<span data-ttu-id="c15ce-115">Essas propriedades especificam o arquivo de recurso que contém um ícone personalizado que representa um provedor MAPI em um estado online, e, opcionalmente, outro ícone personalizado no estado offline.</span><span class="sxs-lookup"><span data-stu-id="c15ce-115">These properties specify the resource file that contains a custom icon that represents a MAPI provider in an online state, and optionally, another custom icon in the offline state.</span></span> <span data-ttu-id="c15ce-116">Outlook sempre solicita essas propriedades na representação Unicode.</span><span class="sxs-lookup"><span data-stu-id="c15ce-116">Outlook always requests these properties in Unicode representation.</span></span> 
  
<span data-ttu-id="c15ce-117">Por exemplo, o valor da propriedade seguir instrui o Outlook carregar ícone 1001 de ID de mymod32.dll o módulo e use esse ícone para o estado online: `mymod32.dll,#1001`.</span><span class="sxs-lookup"><span data-stu-id="c15ce-117">For example, the following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state:  `mymod32.dll,#1001`.</span></span> <span data-ttu-id="c15ce-118">Como não há nenhum ícone específico do provedor para o estado offline, nesse caso, o ícone padrão do Outlook offline é usado na barra de status.</span><span class="sxs-lookup"><span data-stu-id="c15ce-118">Since there is no provider-specific icon for the offline state, in this case, the standard Outlook offline icon is used in the status bar.</span></span> 
  
<span data-ttu-id="c15ce-119">O valor da propriedade seguir instrui o Outlook para carregar ícone 1001 ID do mymod32.dll módulo e use esse ícone para o estado online e também carregar ícone 1002 ID desse mesmo módulo a ser usado para o estado offline: `mymod32.dll,#1001,#1002`.</span><span class="sxs-lookup"><span data-stu-id="c15ce-119">The following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state, and to also load icon ID 1002 from this same module to be used for the offline state:  `mymod32.dll,#1001,#1002`.</span></span> <span data-ttu-id="c15ce-120">Nenhum ícone do Outlook é usado na barra de status.</span><span class="sxs-lookup"><span data-stu-id="c15ce-120">No Outlook icon is used in the status bar.</span></span> 
  
<span data-ttu-id="c15ce-121">Por padrão, se nenhum ícones personalizados forem especificados, o provedor é representado pelos ícones de padrão do Outlook para o estado online e o estado offline.</span><span class="sxs-lookup"><span data-stu-id="c15ce-121">By default, if no custom icons are specified, the provider is represented by the Outlook default icons for the online state and the offline state.</span></span> <span data-ttu-id="c15ce-122">O provedor, opcionalmente, pode especificar um nome de exibição seja mostrado adjacente ao ícone na barra de status.</span><span class="sxs-lookup"><span data-stu-id="c15ce-122">The provider can optionally specify a display name to be shown adjacent to the icon in the status bar.</span></span> <span data-ttu-id="c15ce-123">Para obter mais informações, consulte **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c15ce-123">For more information, see **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c15ce-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c15ce-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c15ce-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c15ce-125">Header files</span></span>

<span data-ttu-id="c15ce-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c15ce-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c15ce-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c15ce-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="c15ce-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c15ce-128">Mapitags.h</span></span>
  
> <span data-ttu-id="c15ce-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c15ce-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c15ce-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c15ce-130">See also</span></span>



[<span data-ttu-id="c15ce-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c15ce-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c15ce-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c15ce-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c15ce-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c15ce-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c15ce-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c15ce-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

