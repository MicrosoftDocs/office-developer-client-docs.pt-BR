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
# <a name="pidtagrenderingposition-canonical-property"></a><span data-ttu-id="81dbc-103">Propriedade canônica PidTagRenderingPosition</span><span class="sxs-lookup"><span data-stu-id="81dbc-103">PidTagRenderingPosition Canonical Property</span></span>

  
  
<span data-ttu-id="81dbc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81dbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81dbc-105">Contém um deslocamento, em caracteres, a ser usado na renderização de um anexo dentro do texto da mensagem principal.</span><span class="sxs-lookup"><span data-stu-id="81dbc-105">Contains an offset, in characters, to use in rendering an attachment within the main message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81dbc-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="81dbc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81dbc-107">PR_RENDERING_POSITION</span><span class="sxs-lookup"><span data-stu-id="81dbc-107">PR_RENDERING_POSITION</span></span>  <br/> |
|<span data-ttu-id="81dbc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="81dbc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="81dbc-109">0x370B</span><span class="sxs-lookup"><span data-stu-id="81dbc-109">0x370B</span></span>  <br/> |
|<span data-ttu-id="81dbc-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="81dbc-110">Data type:</span></span>  <br/> |<span data-ttu-id="81dbc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="81dbc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="81dbc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="81dbc-112">Area:</span></span>  <br/> |<span data-ttu-id="81dbc-113">Anexo MAPI</span><span class="sxs-lookup"><span data-stu-id="81dbc-113">MAPI attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81dbc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="81dbc-114">Remarks</span></span>

<span data-ttu-id="81dbc-115">Quando o deslocamento fornecido é-1 (0xFFFFFFFF), o anexo não é renderizado usando essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="81dbc-115">When the supplied offset is -1 (0xFFFFFFFF), the attachment is not rendered by using this property.</span></span> <span data-ttu-id="81dbc-116">Todos os valores diferentes de-1 indicam a posição dentro da propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) na qual o anexo deve ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="81dbc-116">All values other than -1 indicate the position within the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property at which the attachment is to be rendered.</span></span>
  
 <span data-ttu-id="81dbc-117">**Observação** O caractere indicado por essa propriedade no **PR_BODY** é substituído pelo anexo.</span><span class="sxs-lookup"><span data-stu-id="81dbc-117">**Note** The character indicated by this property in **PR_BODY** is replaced by the attachment.</span></span> <span data-ttu-id="81dbc-118">Normalmente, esse caractere é um espaço, embora um caractere de espaço reservado especial também possa ser usado.</span><span class="sxs-lookup"><span data-stu-id="81dbc-118">Typically this character is a space, although a special placeholder character can also be used.</span></span> 
  
<span data-ttu-id="81dbc-119">Essa propriedade é expressa em caracteres.</span><span class="sxs-lookup"><span data-stu-id="81dbc-119">This property is expressed in characters.</span></span> <span data-ttu-id="81dbc-120">Em alguns conjuntos de caracteres, isso não é equivalente a bytes.</span><span class="sxs-lookup"><span data-stu-id="81dbc-120">In some character sets this is not equivalent to bytes.</span></span> <span data-ttu-id="81dbc-121">Os aplicativos Unicode podem calcular a posição com base em caracteres de dois bytes.</span><span class="sxs-lookup"><span data-stu-id="81dbc-121">Unicode applications can compute the position based on two-byte characters.</span></span> <span data-ttu-id="81dbc-122">Os aplicativos de conjunto de caracteres de dois bytes (DBCS) devem digitalizar o texto até esse valor da propriedade, pois sua representação de caracteres varia entre um e dois bytes por caractere.</span><span class="sxs-lookup"><span data-stu-id="81dbc-122">Double-Byte Character Set (DBCS) applications must scan the text up to this property value, because their character representation varies between one and two bytes per character.</span></span>
  
<span data-ttu-id="81dbc-123">Esta propriedade não deve ser usada com texto Rich Text Format (RTF).</span><span class="sxs-lookup"><span data-stu-id="81dbc-123">This property should not be used with Rich Text Format (RTF) text.</span></span> <span data-ttu-id="81dbc-124">A posição de renderização é indicada em RTF por uma sequência de escape chamada espaço reservado para o objeto Attachment.</span><span class="sxs-lookup"><span data-stu-id="81dbc-124">The rendering position is indicated in RTF by an escape sequence called the object attachment placeholder.</span></span> <span data-ttu-id="81dbc-125">Essa sequência consiste na cadeia de `\objattph` caracteres seguida por um único caractere, normalmente um espaço, que será substituído pela renderização de anexo.</span><span class="sxs-lookup"><span data-stu-id="81dbc-125">This sequence consists of the string  `\objattph` followed by a single character, normally a space, that will be replaced by the attachment rendering.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="81dbc-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="81dbc-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81dbc-127">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="81dbc-127">Protocol specifications</span></span>

<span data-ttu-id="81dbc-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81dbc-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81dbc-129">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="81dbc-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="81dbc-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81dbc-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81dbc-131">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="81dbc-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81dbc-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="81dbc-132">Header files</span></span>

<span data-ttu-id="81dbc-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="81dbc-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="81dbc-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="81dbc-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="81dbc-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="81dbc-135">Mapitags.h</span></span>
  
> <span data-ttu-id="81dbc-136">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="81dbc-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81dbc-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="81dbc-137">See also</span></span>



[<span data-ttu-id="81dbc-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="81dbc-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81dbc-139">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="81dbc-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81dbc-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="81dbc-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81dbc-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="81dbc-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

