---
title: Exemplo de fluxo de PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fc216302cb68be4b0e9d57f60f491adebcba1975
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573926"
---
# <a name="propertydefinition-stream-sample"></a><span data-ttu-id="f2cc4-103">Exemplo de fluxo de PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="f2cc4-103">PropertyDefinition stream sample</span></span>

<span data-ttu-id="f2cc4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2cc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2cc4-105">Este tópico descreve um exemplo de um stream PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-105">This topic describes an example of a PropertyDefinition stream.</span></span> <span data-ttu-id="f2cc4-106">O fluxo contém uma definição de um campo definido pelo usuário, `TextField1`.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="f2cc4-107">O tipo é **texto**e a definição está no formato PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-107">The type is **Text**, and the definition is in the PropDefV2 format.</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="f2cc4-108">Despejo de dados</span><span class="sxs-lookup"><span data-stu-id="f2cc4-108">Data dump</span></span>

<span data-ttu-id="f2cc4-109">A seguir está um despejo do fluxo de dados como ela seria exibida em um editor de binário.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-109">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="f2cc4-110">Deslocamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="f2cc4-110">Stream offset</span></span>|<span data-ttu-id="f2cc4-111">Bytes de dados</span><span class="sxs-lookup"><span data-stu-id="f2cc4-111">Data bytes</span></span>|<span data-ttu-id="f2cc4-112">Dados ASCII</span><span class="sxs-lookup"><span data-stu-id="f2cc4-112">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
<span data-ttu-id="f2cc4-113">A seguir está uma análise dos dados de amostra para o fluxo de PropertyDefinition:</span><span class="sxs-lookup"><span data-stu-id="f2cc4-113">The following is a parse of the sample data for the PropertyDefinition stream:</span></span>
  
- <span data-ttu-id="f2cc4-114">Versão: Deslocamento 0x0, 2 bytes: 0x0103 (PropDefV2).</span><span class="sxs-lookup"><span data-stu-id="f2cc4-114">Version: Offset 0x0, 2 bytes: 0x0103 (PropDefV2).</span></span>
    
- <span data-ttu-id="f2cc4-115">FieldDefinitionCount: Deslocamento 0x2, 4 bytes: 0x1 (1).</span><span class="sxs-lookup"><span data-stu-id="f2cc4-115">FieldDefinitionCount: Offset 0x2, 4 bytes: 0x1 (1).</span></span>
    
- <span data-ttu-id="f2cc4-116">FieldDefinitions: Deslocamento 0x6, matriz de fluxo de FieldDefinition 1.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-116">FieldDefinitions: Offset 0x6, array of 1 FieldDefinition stream.</span></span>
    
  - <span data-ttu-id="f2cc4-117">Sinalizadores: Deslocamento 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).</span><span class="sxs-lookup"><span data-stu-id="f2cc4-117">Flags: Offset 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM|PDO_PRINT_SAVEAS|PDO_PRINT_SAVEAS_DEF).</span></span>
    
  - <span data-ttu-id="f2cc4-118">VT: Deslocamento 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span><span class="sxs-lookup"><span data-stu-id="f2cc4-118">VT: Offset 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span></span>
    
  - <span data-ttu-id="f2cc4-119">DispId: Deslocamento 0xC, 4 bytes: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f2cc4-119">DispId: Offset 0xC, 4 bytes: 0x0 (0).</span></span>
    
  - <span data-ttu-id="f2cc4-120">NmidNameLength: Deslocamento 0x10, 2 bytes: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="f2cc4-120">NmidNameLength: Offset 0x10, 2 bytes: 0xA (10).</span></span>
    
  - <span data-ttu-id="f2cc4-121">NmidName: Deslocamento 0x12, matriz de 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-121">NmidName: Offset 0x12, array of 10 WCHARs.</span></span> <span data-ttu-id="f2cc4-122">Valor de cadeia de caracteres Unicode: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="f2cc4-122">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="f2cc4-123">NameANSI: Deslocamento 0x26, PackedAnsiString stream.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-123">NameANSI: Offset 0x26, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="f2cc4-124">Duração: Deslocamento 0x26, 1 byte: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="f2cc4-124">Length: Offset 0x26, 1 byte: 0xA (10).</span></span>
      
    - <span data-ttu-id="f2cc4-125">Caracteres: Deslocamento 0x27, matriz de 10 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-125">Characters: Offset 0x27, array of 10 CHARs.</span></span> <span data-ttu-id="f2cc4-126">Valor de cadeia de caracteres ANSI: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="f2cc4-126">ANSI string value: "TextField1".</span></span>
    
  - <span data-ttu-id="f2cc4-127">FormulaANSI: Deslocamento 0x31, PackedAnsiString stream.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-127">FormulaANSI: Offset 0x31, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="f2cc4-128">Duração: Deslocamento 0x31, 1 byte: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f2cc4-128">Length: Offset 0x31, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="f2cc4-129">Caracteres: Deslocamento 0x32, matriz de caracteres de 0.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-129">Characters: Offset 0x32, array of 0 CHARs.</span></span> <span data-ttu-id="f2cc4-130">Cadeia de caracteres vazia do ANSI.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-130">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="f2cc4-131">ValidationRuleANSI: Deslocamento 0x32, PackedAnsiString stream.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-131">ValidationRuleANSI: Offset 0x32, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="f2cc4-132">Duração: Deslocamento 0x32, 1 byte: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f2cc4-132">Length: Offset 0x32, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="f2cc4-133">Caracteres: Deslocamento 0x33, matriz de caracteres de 0.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-133">Characters: Offset 0x33, array of 0 CHARs.</span></span> <span data-ttu-id="f2cc4-134">Cadeia de caracteres vazia do ANSI.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-134">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="f2cc4-135">ValidationTextANSI: Deslocamento 0x33, PackedAnsiString stream.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-135">ValidationTextANSI: Offset 0x33, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="f2cc4-136">Duração: Deslocamento 0x33, 1 byte: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f2cc4-136">Length: Offset 0x33, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="f2cc4-137">Caracteres: Deslocamento 0x34, matriz de caracteres de 0.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-137">Characters: Offset 0x34, array of 0 CHARs.</span></span> <span data-ttu-id="f2cc4-138">Cadeia de caracteres vazia do ANSI.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-138">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="f2cc4-139">ErrorANSI: Deslocamento 0x34, PackedAnsiString stream.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-139">ErrorANSI: Offset 0x34, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="f2cc4-140">Duração: Deslocamento 0x34, 1 byte: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f2cc4-140">Length: Offset 0x34, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="f2cc4-141">Caracteres: Deslocamento 0x35, matriz de caracteres de 0.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-141">Characters: Offset 0x35, array of 0 CHARs.</span></span> <span data-ttu-id="f2cc4-142">Cadeia de caracteres vazia do ANSI.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-142">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="f2cc4-143">InternalType: Deslocamento 0x35, 4 bytes: 0x0 (iTypeString).</span><span class="sxs-lookup"><span data-stu-id="f2cc4-143">InternalType: Offset 0x35, 4 bytes: 0x0 (iTypeString).</span></span>
    
  - <span data-ttu-id="f2cc4-144">SkipBlocks: Deslocamento 0x39, série de fluxos de SkipBlock.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-144">SkipBlocks: Offset 0x39, series of SkipBlock streams.</span></span>
    
  - <span data-ttu-id="f2cc4-145">Primeiro SkipBlock</span><span class="sxs-lookup"><span data-stu-id="f2cc4-145">First SkipBlock</span></span>
    
    - <span data-ttu-id="f2cc4-146">Tamanho: Deslocamento 0x39, 4 bytes: 0x15 (21).</span><span class="sxs-lookup"><span data-stu-id="f2cc4-146">Size: Offset 0x39, 4 bytes: 0x15 (21).</span></span>
      
    - <span data-ttu-id="f2cc4-147">Conteúdo: Deslocamento 0x3D, a matriz de bytes 21.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-147">Content: Offset 0x3D, array of 21 bytes.</span></span> <span data-ttu-id="f2cc4-148">Isso é o primeiro fluxo do SkipBlock, essa matriz contém um fluxo de FirstSkipBlockContent.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-148">This is the first SkipBlock stream, so this array contains a FirstSkipBlockContent stream.</span></span>
      
      - <span data-ttu-id="f2cc4-149">FieldName: Deslocamento 0x3D, PackedUnicodeString stream.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-149">FieldName: Offset 0x3D, PackedUnicodeString stream.</span></span>
        
        - <span data-ttu-id="f2cc4-150">Duração: Deslocamento 0x3D, 1 byte: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="f2cc4-150">Length: Offset 0x3D, 1 byte: 0xA (10).</span></span>
          
        - <span data-ttu-id="f2cc4-151">Caracteres: Deslocamento 0x3E, matriz de 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-151">Characters: Offset 0x3E, array of 10 WCHARs.</span></span> <span data-ttu-id="f2cc4-152">Valor de cadeia de caracteres Unicode: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="f2cc4-152">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="f2cc4-153">Segundo SkipBlock</span><span class="sxs-lookup"><span data-stu-id="f2cc4-153">Second SkipBlock</span></span>
    
    - <span data-ttu-id="f2cc4-154">Tamanho: Deslocamento 0x52, 4 bytes: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f2cc4-154">Size: Offset 0x52, 4 bytes: 0x0 (0).</span></span> <span data-ttu-id="f2cc4-155">Este é o fluxo de SkipBlock terminação.</span><span class="sxs-lookup"><span data-stu-id="f2cc4-155">This is the terminating SkipBlock stream.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2cc4-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2cc4-156">See also</span></span>

- [<span data-ttu-id="f2cc4-157">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="f2cc4-157">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="f2cc4-158">Estruturas de fluxo</span><span class="sxs-lookup"><span data-stu-id="f2cc4-158">Stream Structures</span></span>](stream-structures.md)
- [<span data-ttu-id="f2cc4-159">Estrutura de fluxo de PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="f2cc4-159">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="f2cc4-160">Estrutura de fluxo de FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="f2cc4-160">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="f2cc4-161">Estrutura de fluxo de SkipBlock</span><span class="sxs-lookup"><span data-stu-id="f2cc4-161">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="f2cc4-162">Estrutura de fluxo de FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="f2cc4-162">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="f2cc4-163">Estrutura de fluxo de PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="f2cc4-163">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="f2cc4-164">Estrutura de fluxo de PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="f2cc4-164">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

