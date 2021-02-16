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
ms.openlocfilehash: d463be4a14ecf478bdcbddc50b4ad9360829befc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355150"
---
# <a name="pidtagrenderingposition-canonical-property"></a><span data-ttu-id="7ef11-103">Propriedade canônica PidTagRenderingPosition</span><span class="sxs-lookup"><span data-stu-id="7ef11-103">PidTagRenderingPosition Canonical Property</span></span>

  
  
<span data-ttu-id="7ef11-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ef11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ef11-105">Contém um deslocamento, em caracteres, a ser usado na renderização de um anexo no texto da mensagem principal.</span><span class="sxs-lookup"><span data-stu-id="7ef11-105">Contains an offset, in characters, to use in rendering an attachment within the main message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7ef11-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7ef11-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7ef11-107">PR_RENDERING_POSITION</span><span class="sxs-lookup"><span data-stu-id="7ef11-107">PR_RENDERING_POSITION</span></span>  <br/> |
|<span data-ttu-id="7ef11-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7ef11-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7ef11-109">0x370B</span><span class="sxs-lookup"><span data-stu-id="7ef11-109">0x370B</span></span>  <br/> |
|<span data-ttu-id="7ef11-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7ef11-110">Data type:</span></span>  <br/> |<span data-ttu-id="7ef11-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7ef11-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7ef11-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7ef11-112">Area:</span></span>  <br/> |<span data-ttu-id="7ef11-113">Anexo MAPI</span><span class="sxs-lookup"><span data-stu-id="7ef11-113">MAPI attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ef11-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ef11-114">Remarks</span></span>

<span data-ttu-id="7ef11-115">Quando o deslocamento fornecido for -1 (0xFFFFFFFF), o anexo não será renderizado usando essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="7ef11-115">When the supplied offset is -1 (0xFFFFFFFF), the attachment is not rendered by using this property.</span></span> <span data-ttu-id="7ef11-116">Todos os valores diferentes de -1 indicam a posição dentro da propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) na qual o anexo deve ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="7ef11-116">All values other than -1 indicate the position within the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property at which the attachment is to be rendered.</span></span>
  
 <span data-ttu-id="7ef11-117">**Observação** O caractere indicado por essa propriedade **PR_BODY** é substituído pelo anexo.</span><span class="sxs-lookup"><span data-stu-id="7ef11-117">**Note** The character indicated by this property in **PR_BODY** is replaced by the attachment.</span></span> <span data-ttu-id="7ef11-118">Normalmente, esse caractere é um espaço, embora um caractere de espaço reservado especial também possa ser usado.</span><span class="sxs-lookup"><span data-stu-id="7ef11-118">Typically this character is a space, although a special placeholder character can also be used.</span></span> 
  
<span data-ttu-id="7ef11-119">Essa propriedade é expressa em caracteres.</span><span class="sxs-lookup"><span data-stu-id="7ef11-119">This property is expressed in characters.</span></span> <span data-ttu-id="7ef11-120">Em alguns conjuntos de caracteres, isso não é equivalente a bytes.</span><span class="sxs-lookup"><span data-stu-id="7ef11-120">In some character sets this is not equivalent to bytes.</span></span> <span data-ttu-id="7ef11-121">Aplicativos Unicode podem calcular a posição com base em caracteres de dois byte.</span><span class="sxs-lookup"><span data-stu-id="7ef11-121">Unicode applications can compute the position based on two-byte characters.</span></span> <span data-ttu-id="7ef11-122">Double-Byte DBCS (Conjunto de Caracteres) deve examinar o texto até esse valor de propriedade, porque sua representação de caractere varia entre um e dois bytes por caractere.</span><span class="sxs-lookup"><span data-stu-id="7ef11-122">Double-Byte Character Set (DBCS) applications must scan the text up to this property value, because their character representation varies between one and two bytes per character.</span></span>
  
<span data-ttu-id="7ef11-123">Essa propriedade não deve ser usada com texto RTF (Rich Text Format).</span><span class="sxs-lookup"><span data-stu-id="7ef11-123">This property should not be used with Rich Text Format (RTF) text.</span></span> <span data-ttu-id="7ef11-124">A posição de renderização é indicada em RTF por uma sequência de escape chamada de espaço reservado para anexo de objeto.</span><span class="sxs-lookup"><span data-stu-id="7ef11-124">The rendering position is indicated in RTF by an escape sequence called the object attachment placeholder.</span></span> <span data-ttu-id="7ef11-125">Essa sequência consiste na cadeia de caracteres seguida por um único caractere, normalmente um espaço, que será  `\objattph` substituído pela renderização do anexo.</span><span class="sxs-lookup"><span data-stu-id="7ef11-125">This sequence consists of the string  `\objattph` followed by a single character, normally a space, that will be replaced by the attachment rendering.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7ef11-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ef11-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7ef11-127">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="7ef11-127">Protocol specifications</span></span>

<span data-ttu-id="7ef11-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ef11-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7ef11-129">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7ef11-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7ef11-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ef11-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7ef11-131">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="7ef11-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7ef11-132">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="7ef11-132">Header files</span></span>

<span data-ttu-id="7ef11-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7ef11-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="7ef11-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7ef11-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="7ef11-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7ef11-135">Mapitags.h</span></span>
  
> <span data-ttu-id="7ef11-136">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7ef11-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7ef11-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ef11-137">See also</span></span>



[<span data-ttu-id="7ef11-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7ef11-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7ef11-139">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7ef11-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7ef11-140">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7ef11-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7ef11-141">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7ef11-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

