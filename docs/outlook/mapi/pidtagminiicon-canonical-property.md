---
title: Propriedade canônica PidTagMiniIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMiniIcon
api_type:
- HeaderDef
ms.assetid: a436b590-63f3-413c-a9c2-7664567e0ff0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ea7f9e0ed57c56b48399b9ffd1ea42db28daf249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356228"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="8e316-103">Propriedade canônica PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="8e316-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="8e316-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e316-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e316-105">Contém um bitmap de um ícone de meio tamanho de um formulário.</span><span class="sxs-lookup"><span data-stu-id="8e316-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e316-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8e316-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e316-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="8e316-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="8e316-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8e316-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e316-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="8e316-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="8e316-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8e316-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e316-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8e316-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8e316-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8e316-112">Area:</span></span>  <br/> |<span data-ttu-id="8e316-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="8e316-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e316-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e316-114">Remarks</span></span>

<span data-ttu-id="8e316-115">Esta propriedade contém uma imagem de pixel 32 × 32 de um ícone, o mesmo que o conteúdo de um. ICO, mas somente os 16 × 16 pixels superiores são considerados significativos.</span><span class="sxs-lookup"><span data-stu-id="8e316-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="8e316-116">Essa propriedade normalmente é copiada do. ICO especificado na linha SmallIcon da seção [Description] apropriada do arquivo de configuração de formulário.</span><span class="sxs-lookup"><span data-stu-id="8e316-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="8e316-117">**Observação** Algumas plataformas não dão suporte a ícones com 16 × 16 pixels.</span><span class="sxs-lookup"><span data-stu-id="8e316-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="8e316-118">O formato 32 × 32 dessa propriedade pode ser usado nesse caso, mas os aplicativos cliente devem estar cientes das inconsistências de exibição.</span><span class="sxs-lookup"><span data-stu-id="8e316-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8e316-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e316-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8e316-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8e316-120">Header files</span></span>

<span data-ttu-id="8e316-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8e316-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e316-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8e316-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e316-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8e316-123">Mapitags.h</span></span>
  
> <span data-ttu-id="8e316-124">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="8e316-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e316-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e316-125">See also</span></span>



[<span data-ttu-id="8e316-126">Propriedade canônica PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="8e316-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="8e316-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8e316-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e316-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8e316-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e316-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8e316-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e316-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8e316-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

