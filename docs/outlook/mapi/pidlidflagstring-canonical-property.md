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
ms.openlocfilehash: 53fe309fb15807ad698fef5a06781e5c3e0bae0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768476"
---
# <a name="pidlidflagstring-canonical-property"></a><span data-ttu-id="37f6c-103">Propriedade canônica PidLidFlagString</span><span class="sxs-lookup"><span data-stu-id="37f6c-103">PidLidFlagString Canonical Property</span></span>

  
  
<span data-ttu-id="37f6c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="37f6c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="37f6c-105">Contém um índice que identifica um conjunto de cadeias de caracteres de texto predefinido associado com o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="37f6c-105">Contains an index that identifies one of a set of pre-defined text strings associated with the flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37f6c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="37f6c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37f6c-107">dispidFlagStringEnum</span><span class="sxs-lookup"><span data-stu-id="37f6c-107">dispidFlagStringEnum</span></span>  <br/> |
|<span data-ttu-id="37f6c-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="37f6c-108">Property set:</span></span>  <br/> |<span data-ttu-id="37f6c-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="37f6c-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="37f6c-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="37f6c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="37f6c-111">0x000085C0</span><span class="sxs-lookup"><span data-stu-id="37f6c-111">0x000085C0</span></span>  <br/> |
|<span data-ttu-id="37f6c-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="37f6c-112">Data type:</span></span>  <br/> |<span data-ttu-id="37f6c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="37f6c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="37f6c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="37f6c-114">Area:</span></span>  <br/> |<span data-ttu-id="37f6c-115">Task</span><span class="sxs-lookup"><span data-stu-id="37f6c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37f6c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="37f6c-116">Remarks</span></span>

<span data-ttu-id="37f6c-117">Se essa propriedade estiver definida, os clientes devem usar o valor de cadeia de caracteres correspondente nas tabelas a seguir (por exemplo, para substituir uma cadeia de caracteres que é traduzida no idioma do usuário atual) e devem ignorar o valor definido no **dispidFlagRequest** ([ PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) e **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="37f6c-117">If this property is set, clients should use the corresponding string value in the tables below (for example, to substitute a string that is translated into the current user's language), and should ignore the value set in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span></span> 
  
<span data-ttu-id="37f6c-118">Padrões sugeridos para o usuário para objetos de contato são:</span><span class="sxs-lookup"><span data-stu-id="37f6c-118">Defaults suggested to the user for contact objects are as follows:</span></span>
  
|<span data-ttu-id="37f6c-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="37f6c-119">**Value**</span></span>|<span data-ttu-id="37f6c-120">**Cadeia de caracteres de inglês**</span><span class="sxs-lookup"><span data-stu-id="37f6c-120">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37f6c-121">0x00000000 ou não está presente</span><span class="sxs-lookup"><span data-stu-id="37f6c-121">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="37f6c-122">Siga as orientações relacionadas à exibindo **dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="37f6c-122">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="37f6c-123">0x0000006E</span><span class="sxs-lookup"><span data-stu-id="37f6c-123">0x0000006E</span></span>  <br/> |<span data-ttu-id="37f6c-124">"Acompanhamento"</span><span class="sxs-lookup"><span data-stu-id="37f6c-124">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="37f6c-125">0x0000006F</span><span class="sxs-lookup"><span data-stu-id="37f6c-125">0x0000006F</span></span>  <br/> |<span data-ttu-id="37f6c-126">"Chamada"</span><span class="sxs-lookup"><span data-stu-id="37f6c-126">"Call"</span></span>  <br/> |
|<span data-ttu-id="37f6c-127">0x00000070</span><span class="sxs-lookup"><span data-stu-id="37f6c-127">0x00000070</span></span>  <br/> |<span data-ttu-id="37f6c-128">"Organizar reuniões"</span><span class="sxs-lookup"><span data-stu-id="37f6c-128">"Arrange Meeting"</span></span>  <br/> |
|<span data-ttu-id="37f6c-129">0x00000071</span><span class="sxs-lookup"><span data-stu-id="37f6c-129">0x00000071</span></span>  <br/> |<span data-ttu-id="37f6c-130">"Enviar Email"</span><span class="sxs-lookup"><span data-stu-id="37f6c-130">"Send Email"</span></span>  <br/> |
|<span data-ttu-id="37f6c-131">0x00000072</span><span class="sxs-lookup"><span data-stu-id="37f6c-131">0x00000072</span></span>  <br/> |<span data-ttu-id="37f6c-132">"Enviar a letra"</span><span class="sxs-lookup"><span data-stu-id="37f6c-132">"Send Letter"</span></span>  <br/> |
   
<span data-ttu-id="37f6c-133">Padrões sugeridos para o usuário para todos os outros objetos de mensagem são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="37f6c-133">Defaults suggested to the user for all other message objects are as follows:</span></span>
  
|<span data-ttu-id="37f6c-134">**Valor**</span><span class="sxs-lookup"><span data-stu-id="37f6c-134">**Value**</span></span>|<span data-ttu-id="37f6c-135">**Cadeia de caracteres de inglês**</span><span class="sxs-lookup"><span data-stu-id="37f6c-135">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37f6c-136">0x00000000 ou não está presente</span><span class="sxs-lookup"><span data-stu-id="37f6c-136">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="37f6c-137">Siga as orientações relacionadas à exibindo **dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="37f6c-137">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="37f6c-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="37f6c-138">0x00000001</span></span>  <br/> |<span data-ttu-id="37f6c-139">"Chamada"</span><span class="sxs-lookup"><span data-stu-id="37f6c-139">"Call"</span></span>  <br/> |
|<span data-ttu-id="37f6c-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="37f6c-140">0x00000002</span></span>  <br/> |<span data-ttu-id="37f6c-141">"Não encaminhar"</span><span class="sxs-lookup"><span data-stu-id="37f6c-141">"Do not Forward"</span></span>  <br/> |
|<span data-ttu-id="37f6c-142">0x00000003</span><span class="sxs-lookup"><span data-stu-id="37f6c-142">0x00000003</span></span>  <br/> |<span data-ttu-id="37f6c-143">"Acompanhamento"</span><span class="sxs-lookup"><span data-stu-id="37f6c-143">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="37f6c-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="37f6c-144">0x00000004</span></span>  <br/> |<span data-ttu-id="37f6c-145">"Para sua informação"</span><span class="sxs-lookup"><span data-stu-id="37f6c-145">"For Your Information"</span></span>  <br/> |
|<span data-ttu-id="37f6c-146">0x00000005</span><span class="sxs-lookup"><span data-stu-id="37f6c-146">0x00000005</span></span>  <br/> |<span data-ttu-id="37f6c-147">"Encaminhar"</span><span class="sxs-lookup"><span data-stu-id="37f6c-147">"Forward"</span></span>  <br/> |
|<span data-ttu-id="37f6c-148">0x00000006</span><span class="sxs-lookup"><span data-stu-id="37f6c-148">0x00000006</span></span>  <br/> |<span data-ttu-id="37f6c-149">"Não é preciso responder"</span><span class="sxs-lookup"><span data-stu-id="37f6c-149">"No Response Necessary"</span></span>  <br/> |
|<span data-ttu-id="37f6c-150">0x00000007</span><span class="sxs-lookup"><span data-stu-id="37f6c-150">0x00000007</span></span>  <br/> |<span data-ttu-id="37f6c-151">"Ler"</span><span class="sxs-lookup"><span data-stu-id="37f6c-151">"Read"</span></span>  <br/> |
|<span data-ttu-id="37f6c-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="37f6c-152">0x00000008</span></span>  <br/> |<span data-ttu-id="37f6c-153">"Reply"</span><span class="sxs-lookup"><span data-stu-id="37f6c-153">"Reply"</span></span>  <br/> |
|<span data-ttu-id="37f6c-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="37f6c-154">0x00000009</span></span>  <br/> |<span data-ttu-id="37f6c-155">"Responder a todos os"</span><span class="sxs-lookup"><span data-stu-id="37f6c-155">"Reply to All"</span></span>  <br/> |
|<span data-ttu-id="37f6c-156">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="37f6c-156">0x0000000A</span></span>  <br/> |<span data-ttu-id="37f6c-157">"Revisão"</span><span class="sxs-lookup"><span data-stu-id="37f6c-157">"Review"</span></span>  <br/> |
   
<span data-ttu-id="37f6c-158">Todas as cadeias de caracteres especificadas acima podem ser traduzidas para o idioma do usuário, se apropriado.</span><span class="sxs-lookup"><span data-stu-id="37f6c-158">All strings specified above can be translated to the user's language, if appropriate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="37f6c-159">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="37f6c-159">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="37f6c-160">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="37f6c-160">Protocol specifications</span></span>

<span data-ttu-id="37f6c-161">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37f6c-161">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37f6c-162">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="37f6c-162">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="37f6c-163">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37f6c-163">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37f6c-164">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="37f6c-164">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="37f6c-165">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="37f6c-165">Header files</span></span>

<span data-ttu-id="37f6c-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="37f6c-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="37f6c-167">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="37f6c-167">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37f6c-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="37f6c-168">See also</span></span>



[<span data-ttu-id="37f6c-169">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="37f6c-169">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37f6c-170">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="37f6c-170">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37f6c-171">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="37f6c-171">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37f6c-172">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="37f6c-172">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

