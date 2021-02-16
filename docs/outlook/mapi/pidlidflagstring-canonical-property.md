---
title: Propriedade canônica PidLidFlagString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagString
api_type:
- COM
ms.assetid: 4cf1e08b-c869-4965-a1e4-512a0684700f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b3cd88db7e93b53990cf0181af623ebca75f0c6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357782"
---
# <a name="pidlidflagstring-canonical-property"></a><span data-ttu-id="ea682-103">Propriedade canônica PidLidFlagString</span><span class="sxs-lookup"><span data-stu-id="ea682-103">PidLidFlagString Canonical Property</span></span>

  
  
<span data-ttu-id="ea682-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea682-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea682-105">Contém um índice que identifica um de um conjunto de cadeias de caracteres de texto pré-definidas associadas ao sinalizador.</span><span class="sxs-lookup"><span data-stu-id="ea682-105">Contains an index that identifies one of a set of pre-defined text strings associated with the flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ea682-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ea682-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ea682-107">dispidFlagStringEnum</span><span class="sxs-lookup"><span data-stu-id="ea682-107">dispidFlagStringEnum</span></span>  <br/> |
|<span data-ttu-id="ea682-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="ea682-108">Property set:</span></span>  <br/> |<span data-ttu-id="ea682-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ea682-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ea682-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ea682-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ea682-111">0x000085C0</span><span class="sxs-lookup"><span data-stu-id="ea682-111">0x000085C0</span></span>  <br/> |
|<span data-ttu-id="ea682-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ea682-112">Data type:</span></span>  <br/> |<span data-ttu-id="ea682-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ea682-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ea682-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ea682-114">Area:</span></span>  <br/> |<span data-ttu-id="ea682-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="ea682-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea682-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea682-116">Remarks</span></span>

<span data-ttu-id="ea682-117">Se essa propriedade for definida, os clientes deverão usar o valor de cadeia de caracteres correspondente nas tabelas abaixo (por exemplo, para substituir uma cadeia de caracteres traduzida no idioma do usuário atual) e devem ignorar o valor definido em **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) e **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ea682-117">If this property is set, clients should use the corresponding string value in the tables below (for example, to substitute a string that is translated into the current user's language), and should ignore the value set in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span></span> 
  
<span data-ttu-id="ea682-118">Os padrões sugeridos para o usuário para objetos de contato são:</span><span class="sxs-lookup"><span data-stu-id="ea682-118">Defaults suggested to the user for contact objects are as follows:</span></span>
  
|<span data-ttu-id="ea682-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ea682-119">**Value**</span></span>|<span data-ttu-id="ea682-120">**Cadeia de caracteres em inglês**</span><span class="sxs-lookup"><span data-stu-id="ea682-120">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ea682-121">0x00000000 ou não está presente</span><span class="sxs-lookup"><span data-stu-id="ea682-121">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="ea682-122">Siga as orientações relacionadas à **exibição de dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="ea682-122">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="ea682-123">0x0000006E</span><span class="sxs-lookup"><span data-stu-id="ea682-123">0x0000006E</span></span>  <br/> |<span data-ttu-id="ea682-124">"Acompanhamento"</span><span class="sxs-lookup"><span data-stu-id="ea682-124">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="ea682-125">0x0000006F</span><span class="sxs-lookup"><span data-stu-id="ea682-125">0x0000006F</span></span>  <br/> |<span data-ttu-id="ea682-126">"Call"</span><span class="sxs-lookup"><span data-stu-id="ea682-126">"Call"</span></span>  <br/> |
|<span data-ttu-id="ea682-127">0x00000070</span><span class="sxs-lookup"><span data-stu-id="ea682-127">0x00000070</span></span>  <br/> |<span data-ttu-id="ea682-128">"Organizar reunião"</span><span class="sxs-lookup"><span data-stu-id="ea682-128">"Arrange Meeting"</span></span>  <br/> |
|<span data-ttu-id="ea682-129">0x00000071</span><span class="sxs-lookup"><span data-stu-id="ea682-129">0x00000071</span></span>  <br/> |<span data-ttu-id="ea682-130">"Enviar Email"</span><span class="sxs-lookup"><span data-stu-id="ea682-130">"Send Email"</span></span>  <br/> |
|<span data-ttu-id="ea682-131">0x00000072</span><span class="sxs-lookup"><span data-stu-id="ea682-131">0x00000072</span></span>  <br/> |<span data-ttu-id="ea682-132">"Enviar Carta"</span><span class="sxs-lookup"><span data-stu-id="ea682-132">"Send Letter"</span></span>  <br/> |
   
<span data-ttu-id="ea682-133">Os padrões sugeridos para o usuário para todos os outros objetos de mensagem são:</span><span class="sxs-lookup"><span data-stu-id="ea682-133">Defaults suggested to the user for all other message objects are as follows:</span></span>
  
|<span data-ttu-id="ea682-134">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ea682-134">**Value**</span></span>|<span data-ttu-id="ea682-135">**Cadeia de caracteres em inglês**</span><span class="sxs-lookup"><span data-stu-id="ea682-135">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ea682-136">0x00000000 ou não está presente</span><span class="sxs-lookup"><span data-stu-id="ea682-136">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="ea682-137">Siga as orientações relacionadas à **exibição de dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="ea682-137">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="ea682-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ea682-138">0x00000001</span></span>  <br/> |<span data-ttu-id="ea682-139">"Call"</span><span class="sxs-lookup"><span data-stu-id="ea682-139">"Call"</span></span>  <br/> |
|<span data-ttu-id="ea682-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ea682-140">0x00000002</span></span>  <br/> |<span data-ttu-id="ea682-141">"Não Encaminhar"</span><span class="sxs-lookup"><span data-stu-id="ea682-141">"Do not Forward"</span></span>  <br/> |
|<span data-ttu-id="ea682-142">0x00000003</span><span class="sxs-lookup"><span data-stu-id="ea682-142">0x00000003</span></span>  <br/> |<span data-ttu-id="ea682-143">"Acompanhamento"</span><span class="sxs-lookup"><span data-stu-id="ea682-143">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="ea682-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ea682-144">0x00000004</span></span>  <br/> |<span data-ttu-id="ea682-145">"Para suas informações"</span><span class="sxs-lookup"><span data-stu-id="ea682-145">"For Your Information"</span></span>  <br/> |
|<span data-ttu-id="ea682-146">0x00000005</span><span class="sxs-lookup"><span data-stu-id="ea682-146">0x00000005</span></span>  <br/> |<span data-ttu-id="ea682-147">"Encaminhar"</span><span class="sxs-lookup"><span data-stu-id="ea682-147">"Forward"</span></span>  <br/> |
|<span data-ttu-id="ea682-148">0x00000006</span><span class="sxs-lookup"><span data-stu-id="ea682-148">0x00000006</span></span>  <br/> |<span data-ttu-id="ea682-149">"Nenhuma resposta necessária"</span><span class="sxs-lookup"><span data-stu-id="ea682-149">"No Response Necessary"</span></span>  <br/> |
|<span data-ttu-id="ea682-150">0x00000007</span><span class="sxs-lookup"><span data-stu-id="ea682-150">0x00000007</span></span>  <br/> |<span data-ttu-id="ea682-151">"Leitura"</span><span class="sxs-lookup"><span data-stu-id="ea682-151">"Read"</span></span>  <br/> |
|<span data-ttu-id="ea682-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ea682-152">0x00000008</span></span>  <br/> |<span data-ttu-id="ea682-153">"Responder"</span><span class="sxs-lookup"><span data-stu-id="ea682-153">"Reply"</span></span>  <br/> |
|<span data-ttu-id="ea682-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="ea682-154">0x00000009</span></span>  <br/> |<span data-ttu-id="ea682-155">"Responder a Todos"</span><span class="sxs-lookup"><span data-stu-id="ea682-155">"Reply to All"</span></span>  <br/> |
|<span data-ttu-id="ea682-156">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="ea682-156">0x0000000A</span></span>  <br/> |<span data-ttu-id="ea682-157">"Revisão"</span><span class="sxs-lookup"><span data-stu-id="ea682-157">"Review"</span></span>  <br/> |
   
<span data-ttu-id="ea682-158">Todas as cadeias de caracteres especificadas acima podem ser traduzidas para o idioma do usuário, se apropriado.</span><span class="sxs-lookup"><span data-stu-id="ea682-158">All strings specified above can be translated to the user's language, if appropriate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ea682-159">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea682-159">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ea682-160">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ea682-160">Protocol specifications</span></span>

<span data-ttu-id="ea682-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea682-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea682-162">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ea682-162">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ea682-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea682-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea682-164">Especifica as propriedades e operações relacionadas à sinalização.</span><span class="sxs-lookup"><span data-stu-id="ea682-164">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ea682-165">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="ea682-165">Header files</span></span>

<span data-ttu-id="ea682-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ea682-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="ea682-167">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ea682-167">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea682-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea682-168">See also</span></span>



[<span data-ttu-id="ea682-169">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ea682-169">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ea682-170">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ea682-170">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ea682-171">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ea682-171">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ea682-172">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ea682-172">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

