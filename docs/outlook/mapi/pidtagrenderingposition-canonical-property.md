---
title: Propriedade canônica PidTagRenderingPosition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRenderingPosition
api_type:
- COM
ms.assetid: bce46687-17dc-4a3f-96be-303d8755158e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aa149a81102a4981712ea3ca897d8b1ad448a1eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769824"
---
# <a name="pidtagrenderingposition-canonical-property"></a><span data-ttu-id="44f69-103">Propriedade canônica PidTagRenderingPosition</span><span class="sxs-lookup"><span data-stu-id="44f69-103">PidTagRenderingPosition Canonical Property</span></span>

  
  
<span data-ttu-id="44f69-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44f69-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44f69-105">Contém um deslocamento, em caracteres, a ser usado na renderização de um anexo dentro do texto da mensagem principal.</span><span class="sxs-lookup"><span data-stu-id="44f69-105">Contains an offset, in characters, to use in rendering an attachment within the main message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44f69-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="44f69-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44f69-107">PR_RENDERING_POSITION</span><span class="sxs-lookup"><span data-stu-id="44f69-107">PR_RENDERING_POSITION</span></span>  <br/> |
|<span data-ttu-id="44f69-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="44f69-108">Identifier:</span></span>  <br/> |<span data-ttu-id="44f69-109">0x370B</span><span class="sxs-lookup"><span data-stu-id="44f69-109">0x370B</span></span>  <br/> |
|<span data-ttu-id="44f69-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="44f69-110">Data type:</span></span>  <br/> |<span data-ttu-id="44f69-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="44f69-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="44f69-112">Área:</span><span class="sxs-lookup"><span data-stu-id="44f69-112">Area:</span></span>  <br/> |<span data-ttu-id="44f69-113">Anexo MAPI</span><span class="sxs-lookup"><span data-stu-id="44f69-113">MAPI attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44f69-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="44f69-114">Remarks</span></span>

<span data-ttu-id="44f69-115">Quando o deslocamento fornecido é -1 (0xFFFFFFFF), o anexo não é processado usando essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="44f69-115">When the supplied offset is -1 (0xFFFFFFFF), the attachment is not rendered by using this property.</span></span> <span data-ttu-id="44f69-116">Todos os valores que não seja de -1 indicam a posição dentro da propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) em que o anexo é a ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="44f69-116">All values other than -1 indicate the position within the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property at which the attachment is to be rendered.</span></span>
  
 <span data-ttu-id="44f69-117">**Observação** O caractere indicado por esta propriedade em **PR_BODY** é substituído pelo anexo.</span><span class="sxs-lookup"><span data-stu-id="44f69-117">**Note** The character indicated by this property in **PR_BODY** is replaced by the attachment.</span></span> <span data-ttu-id="44f69-118">Geralmente esse caractere é um espaço, embora um caractere de espaço reservado especial também pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="44f69-118">Typically this character is a space, although a special placeholder character can also be used.</span></span> 
  
<span data-ttu-id="44f69-119">Essa propriedade é expresso em caracteres.</span><span class="sxs-lookup"><span data-stu-id="44f69-119">This property is expressed in characters.</span></span> <span data-ttu-id="44f69-120">Em alguns conjuntos de caracteres isso não é equivalente à bytes.</span><span class="sxs-lookup"><span data-stu-id="44f69-120">In some character sets this is not equivalent to bytes.</span></span> <span data-ttu-id="44f69-121">Aplicativos Unicode poderá computar a posição com base em caracteres de dois bytes.</span><span class="sxs-lookup"><span data-stu-id="44f69-121">Unicode applications can compute the position based on two-byte characters.</span></span> <span data-ttu-id="44f69-122">Aplicativos do conjunto de caracteres de Byte duplo (DBCS) devem examinar o texto até o valor dessa propriedade, como sua representação de caracteres varia entre um e dois bytes por caractere.</span><span class="sxs-lookup"><span data-stu-id="44f69-122">Double-Byte Character Set (DBCS) applications must scan the text up to this property value, because their character representation varies between one and two bytes per character.</span></span>
  
<span data-ttu-id="44f69-123">Essa propriedade não deve ser usada com o texto de formato Rich Text (RTF).</span><span class="sxs-lookup"><span data-stu-id="44f69-123">This property should not be used with Rich Text Format (RTF) text.</span></span> <span data-ttu-id="44f69-124">A posição de renderização é indicada em RTF por uma sequência de escape chamada o espaço reservado do objeto attachment.</span><span class="sxs-lookup"><span data-stu-id="44f69-124">The rendering position is indicated in RTF by an escape sequence called the object attachment placeholder.</span></span> <span data-ttu-id="44f69-125">Esta sequência consiste a cadeia de caracteres `\objattph` seguido de um único caractere, normalmente um espaço, que será substituído pela renderização de anexo.</span><span class="sxs-lookup"><span data-stu-id="44f69-125">This sequence consists of the string  `\objattph` followed by a single character, normally a space, that will be replaced by the attachment rendering.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="44f69-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="44f69-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="44f69-127">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="44f69-127">Protocol specifications</span></span>

<span data-ttu-id="44f69-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44f69-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44f69-129">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="44f69-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="44f69-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44f69-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44f69-131">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="44f69-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="44f69-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="44f69-132">Header files</span></span>

<span data-ttu-id="44f69-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44f69-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="44f69-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="44f69-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="44f69-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="44f69-135">Mapitags.h</span></span>
  
> <span data-ttu-id="44f69-136">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="44f69-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44f69-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="44f69-137">See also</span></span>



[<span data-ttu-id="44f69-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="44f69-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44f69-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="44f69-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44f69-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="44f69-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44f69-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="44f69-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

