---
title: Exemplo de fluxo PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 63a8141221c0ff7a8c6ffee20587b682386f87b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406658"
---
# <a name="propertydefinition-stream-sample"></a><span data-ttu-id="836c8-103">Exemplo de fluxo PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="836c8-103">PropertyDefinition stream sample</span></span>

<span data-ttu-id="836c8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="836c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="836c8-105">Este tópico descreve um exemplo de um fluxo PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="836c8-105">This topic describes an example of a PropertyDefinition stream.</span></span> <span data-ttu-id="836c8-106">O fluxo contém uma definição de um campo definido pelo usuário,  `TextField1` .</span><span class="sxs-lookup"><span data-stu-id="836c8-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="836c8-107">O tipo é **Texto** e a definição está no formato PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="836c8-107">The type is **Text**, and the definition is in the PropDefV2 format.</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="836c8-108">Despejo de dados</span><span class="sxs-lookup"><span data-stu-id="836c8-108">Data dump</span></span>

<span data-ttu-id="836c8-109">A seguir está um despejo de dados do fluxo, como seria exibido em um editor binário.</span><span class="sxs-lookup"><span data-stu-id="836c8-109">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="836c8-110">Deslocamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="836c8-110">Stream offset</span></span>|<span data-ttu-id="836c8-111">Bytes de dados</span><span class="sxs-lookup"><span data-stu-id="836c8-111">Data bytes</span></span>|<span data-ttu-id="836c8-112">Dados ASCII</span><span class="sxs-lookup"><span data-stu-id="836c8-112">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
<span data-ttu-id="836c8-113">Veja a seguir uma análise dos dados de exemplo para o fluxo PropertyDefinition:</span><span class="sxs-lookup"><span data-stu-id="836c8-113">The following is a parse of the sample data for the PropertyDefinition stream:</span></span>
  
- <span data-ttu-id="836c8-114">Versão: Deslocamento 0x0, 2 bytes: 0x0103 (PropDefV2).</span><span class="sxs-lookup"><span data-stu-id="836c8-114">Version: Offset 0x0, 2 bytes: 0x0103 (PropDefV2).</span></span>
    
- <span data-ttu-id="836c8-115">FieldDefinitionCount: deslocamento 0x2, 4 bytes: 0x1 (1).</span><span class="sxs-lookup"><span data-stu-id="836c8-115">FieldDefinitionCount: Offset 0x2, 4 bytes: 0x1 (1).</span></span>
    
- <span data-ttu-id="836c8-116">FieldDefinitions: Deslocamento 0x6, matriz de 1 fluxo FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="836c8-116">FieldDefinitions: Offset 0x6, array of 1 FieldDefinition stream.</span></span>
    
  - <span data-ttu-id="836c8-117">Sinalizadores: Deslocamento 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM| PDO_PRINT_SAVEAS| PDO_PRINT_SAVEAS_DEF).</span><span class="sxs-lookup"><span data-stu-id="836c8-117">Flags: Offset 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM|PDO_PRINT_SAVEAS|PDO_PRINT_SAVEAS_DEF).</span></span>
    
  - <span data-ttu-id="836c8-118">VT: deslocamento 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span><span class="sxs-lookup"><span data-stu-id="836c8-118">VT: Offset 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span></span>
    
  - <span data-ttu-id="836c8-119">DispId: deslocamento 0xC, 4 bytes: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="836c8-119">DispId: Offset 0xC, 4 bytes: 0x0 (0).</span></span>
    
  - <span data-ttu-id="836c8-120">NmidNameLength: deslocamento 0x10, 2 bytes: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="836c8-120">NmidNameLength: Offset 0x10, 2 bytes: 0xA (10).</span></span>
    
  - <span data-ttu-id="836c8-121">NmidName: deslocamento 0x12, matriz de 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="836c8-121">NmidName: Offset 0x12, array of 10 WCHARs.</span></span> <span data-ttu-id="836c8-122">Valor da cadeia de caracteres Unicode: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="836c8-122">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="836c8-123">NameANSI: deslocamento 0x26, fluxo PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="836c8-123">NameANSI: Offset 0x26, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="836c8-124">Comprimento: deslocamento 0x26, 1 byte: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="836c8-124">Length: Offset 0x26, 1 byte: 0xA (10).</span></span>
      
    - <span data-ttu-id="836c8-125">Caracteres: Deslocamento 0x27, matriz de 10 CHARs.</span><span class="sxs-lookup"><span data-stu-id="836c8-125">Characters: Offset 0x27, array of 10 CHARs.</span></span> <span data-ttu-id="836c8-126">Valor da cadeia de caracteres ANSI: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="836c8-126">ANSI string value: "TextField1".</span></span>
    
  - <span data-ttu-id="836c8-127">FormulaANSI: deslocamento 0x31, fluxo PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="836c8-127">FormulaANSI: Offset 0x31, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="836c8-128">Comprimento: deslocamento 0x31, 1 byte: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="836c8-128">Length: Offset 0x31, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="836c8-129">Caracteres: Deslocamento 0x32, matriz de 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="836c8-129">Characters: Offset 0x32, array of 0 CHARs.</span></span> <span data-ttu-id="836c8-130">Cadeia de caracteres ANSI vazia.</span><span class="sxs-lookup"><span data-stu-id="836c8-130">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="836c8-131">ValidationRuleANSI: deslocamento 0x32, fluxo PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="836c8-131">ValidationRuleANSI: Offset 0x32, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="836c8-132">Comprimento: deslocamento 0x32, 1 byte: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="836c8-132">Length: Offset 0x32, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="836c8-133">Caracteres: Deslocamento 0x33, matriz de 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="836c8-133">Characters: Offset 0x33, array of 0 CHARs.</span></span> <span data-ttu-id="836c8-134">Cadeia de caracteres ANSI vazia.</span><span class="sxs-lookup"><span data-stu-id="836c8-134">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="836c8-135">ValidationTextANSI: deslocamento 0x33, fluxo PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="836c8-135">ValidationTextANSI: Offset 0x33, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="836c8-136">Comprimento: deslocamento 0x33, 1 byte: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="836c8-136">Length: Offset 0x33, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="836c8-137">Caracteres: Deslocamento 0x34, matriz de 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="836c8-137">Characters: Offset 0x34, array of 0 CHARs.</span></span> <span data-ttu-id="836c8-138">Cadeia de caracteres ANSI vazia.</span><span class="sxs-lookup"><span data-stu-id="836c8-138">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="836c8-139">ErrorANSI: deslocamento 0x34, fluxo PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="836c8-139">ErrorANSI: Offset 0x34, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="836c8-140">Comprimento: deslocamento 0x34, 1 byte: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="836c8-140">Length: Offset 0x34, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="836c8-141">Caracteres: Deslocamento 0x35, matriz de 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="836c8-141">Characters: Offset 0x35, array of 0 CHARs.</span></span> <span data-ttu-id="836c8-142">Cadeia de caracteres ANSI vazia.</span><span class="sxs-lookup"><span data-stu-id="836c8-142">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="836c8-143">InternalType: deslocamento 0x35, 4 bytes: 0x0 (iTypeString).</span><span class="sxs-lookup"><span data-stu-id="836c8-143">InternalType: Offset 0x35, 4 bytes: 0x0 (iTypeString).</span></span>
    
  - <span data-ttu-id="836c8-144">SkipBlocks: Deslocamento 0x39, série de fluxos SkipBlock.</span><span class="sxs-lookup"><span data-stu-id="836c8-144">SkipBlocks: Offset 0x39, series of SkipBlock streams.</span></span>
    
  - <span data-ttu-id="836c8-145">First SkipBlock</span><span class="sxs-lookup"><span data-stu-id="836c8-145">First SkipBlock</span></span>
    
    - <span data-ttu-id="836c8-146">Tamanho: deslocamento 0x39, 4 bytes: 0x15 (21).</span><span class="sxs-lookup"><span data-stu-id="836c8-146">Size: Offset 0x39, 4 bytes: 0x15 (21).</span></span>
      
    - <span data-ttu-id="836c8-147">Conteúdo: deslocamento 0x3D, matriz de 21 bytes.</span><span class="sxs-lookup"><span data-stu-id="836c8-147">Content: Offset 0x3D, array of 21 bytes.</span></span> <span data-ttu-id="836c8-148">Este é o primeiro fluxo SkipBlock, portanto, essa matriz contém um fluxo FirstSkipBlockContent.</span><span class="sxs-lookup"><span data-stu-id="836c8-148">This is the first SkipBlock stream, so this array contains a FirstSkipBlockContent stream.</span></span>
      
      - <span data-ttu-id="836c8-149">FieldName: deslocamento 0x3D, fluxo PackedUnicodeString.</span><span class="sxs-lookup"><span data-stu-id="836c8-149">FieldName: Offset 0x3D, PackedUnicodeString stream.</span></span>
        
        - <span data-ttu-id="836c8-150">Comprimento: deslocamento 0x3D, 1 byte: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="836c8-150">Length: Offset 0x3D, 1 byte: 0xA (10).</span></span>
          
        - <span data-ttu-id="836c8-151">Caracteres: deslocamento 0x3E, matriz de 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="836c8-151">Characters: Offset 0x3E, array of 10 WCHARs.</span></span> <span data-ttu-id="836c8-152">Valor da cadeia de caracteres Unicode: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="836c8-152">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="836c8-153">Segundo SkipBlock</span><span class="sxs-lookup"><span data-stu-id="836c8-153">Second SkipBlock</span></span>
    
    - <span data-ttu-id="836c8-154">Tamanho: deslocamento 0x52, 4 bytes: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="836c8-154">Size: Offset 0x52, 4 bytes: 0x0 (0).</span></span> <span data-ttu-id="836c8-155">Este é o fluxo SkipBlock de encerramento.</span><span class="sxs-lookup"><span data-stu-id="836c8-155">This is the terminating SkipBlock stream.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="836c8-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="836c8-156">See also</span></span>

- [<span data-ttu-id="836c8-157">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="836c8-157">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="836c8-158">Estruturas de fluxo</span><span class="sxs-lookup"><span data-stu-id="836c8-158">Stream Structures</span></span>](stream-structures.md)
- [<span data-ttu-id="836c8-159">Estrutura de fluxo PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="836c8-159">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="836c8-160">Estrutura de Fluxo de FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="836c8-160">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="836c8-161">Estrutura de fluxo SkipBlock</span><span class="sxs-lookup"><span data-stu-id="836c8-161">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="836c8-162">Estrutura de fluxo firstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="836c8-162">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="836c8-163">Estrutura de fluxo de PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="836c8-163">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="836c8-164">Estrutura de fluxo de PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="836c8-164">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

