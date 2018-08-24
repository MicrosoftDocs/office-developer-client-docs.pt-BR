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
ms.openlocfilehash: 5514e0553f719e2e875aad7001bb38a6a52e8e08
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589774"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="020b1-103">Propriedade canônica PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="020b1-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="020b1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="020b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="020b1-105">Contém um bitmap de um ícone de meia largura para um formulário.</span><span class="sxs-lookup"><span data-stu-id="020b1-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="020b1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="020b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="020b1-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="020b1-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="020b1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="020b1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="020b1-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="020b1-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="020b1-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="020b1-110">Data type:</span></span>  <br/> |<span data-ttu-id="020b1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="020b1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="020b1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="020b1-112">Area:</span></span>  <br/> |<span data-ttu-id="020b1-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="020b1-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="020b1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="020b1-114">Remarks</span></span>

<span data-ttu-id="020b1-115">Essa propriedade contém uma imagem de 32 × 32 pixels de um ícone, o mesmo que o conteúdo de um. Arquivo ICO, mas apenas os pixels da parte superior esquerda 16 × 16 são considerados significativa.</span><span class="sxs-lookup"><span data-stu-id="020b1-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="020b1-116">Essa propriedade normalmente é copiada do. Arquivo ICO especificado na linha SmallIcon da seção apropriada [descrição] do arquivo de configuração de formulário.</span><span class="sxs-lookup"><span data-stu-id="020b1-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="020b1-117">**Observação** Algumas plataformas fazer não o suporte a 16 × 16 pixels ícones.</span><span class="sxs-lookup"><span data-stu-id="020b1-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="020b1-118">O formato de 32 × 32 dessa propriedade é utilizável nesse caso, mas os aplicativos cliente devem estar cientes de inconsistências de exibição.</span><span class="sxs-lookup"><span data-stu-id="020b1-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="020b1-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="020b1-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="020b1-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="020b1-120">Header files</span></span>

<span data-ttu-id="020b1-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="020b1-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="020b1-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="020b1-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="020b1-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="020b1-123">Mapitags.h</span></span>
  
> <span data-ttu-id="020b1-124">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="020b1-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="020b1-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="020b1-125">See also</span></span>



[<span data-ttu-id="020b1-126">Propriedade canônica PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="020b1-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="020b1-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="020b1-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="020b1-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="020b1-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="020b1-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="020b1-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="020b1-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="020b1-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

