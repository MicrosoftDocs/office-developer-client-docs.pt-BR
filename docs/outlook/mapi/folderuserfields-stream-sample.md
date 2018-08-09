---
title: Exemplo de fluxo de FolderUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 72c71a6109f55f7ec06499e214a1aa11292a9e52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766571"
---
# <a name="folderuserfields-stream-sample"></a><span data-ttu-id="270b4-103">Exemplo de fluxo de FolderUserFields</span><span class="sxs-lookup"><span data-stu-id="270b4-103">FolderUserFields stream sample</span></span>

<span data-ttu-id="270b4-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="270b4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="270b4-105">Este tópico descreve um exemplo de um fluxo de FolderUserFields.</span><span class="sxs-lookup"><span data-stu-id="270b4-105">This topic describes an example of a FolderUserFields stream.</span></span> <span data-ttu-id="270b4-106">O fluxo contém uma definição de um campo definido pelo usuário, `TextField1`.</span><span class="sxs-lookup"><span data-stu-id="270b4-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="270b4-107">O tipo é **texto**e o fluxo de FolderUserFields contém FolderUserFieldsAnsi e o FolderUserFieldsUnicode partes.</span><span class="sxs-lookup"><span data-stu-id="270b4-107">The type is **Text**, and the FolderUserFields stream contains both FolderUserFieldsAnsi and FolderUserFieldsUnicode parts.</span></span> <span data-ttu-id="270b4-108">Para obter mais informações, consulte [Estruturas de fluxo de campos de pastas](folder-fields-stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="270b4-108">For more information see [Folder Fields Stream Structures](folder-fields-stream-structures.md).</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="270b4-109">Despejo de dados</span><span class="sxs-lookup"><span data-stu-id="270b4-109">Data dump</span></span>

<span data-ttu-id="270b4-110">A seguir está um despejo do fluxo de dados como ela seria exibida em um editor de binário.</span><span class="sxs-lookup"><span data-stu-id="270b4-110">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="270b4-111">Deslocamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="270b4-111">Stream offset</span></span>|<span data-ttu-id="270b4-112">Bytes de dados</span><span class="sxs-lookup"><span data-stu-id="270b4-112">Data bytes</span></span>|<span data-ttu-id="270b4-113">Dados ASCII</span><span class="sxs-lookup"><span data-stu-id="270b4-113">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `02 00 00 00 01 00 00 00 0A 00 54 65 78 74 46 69` <br/> | `..........TextFi` <br/> |
| `0000000010` <br/> | `65 6C 64 31 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `eld1).......A...` <br/> |
| `0000000020` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `0000000030` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000040` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000050` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000060` <br/> | `00 00 00 00 00 00 02 00 00 00 01 00 00 00 0A 00` <br/> | `................` <br/> |
| `0000000070` <br/> | `54 00 65 00 78 00 74 00 46 00 69 00 65 00 6C 00` <br/> | `T.e.x.t.F.i.e.l.` <br/> |
| `0000000080` <br/> | `64 00 31 00 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `d.1.).......A...` <br/> |
| `0000000090` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `00000000A0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000B0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000C0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000D0` <br/> | `00 00 00 00 00 00` <br/> | `......` <br/> |
   

<span data-ttu-id="270b4-114">A seguir está uma análise dos dados de amostra para o fluxo de **FolderUserFields** :</span><span class="sxs-lookup"><span data-stu-id="270b4-114">The following is a parse of the sample data for the **FolderUserFields** stream:</span></span>
  
- <span data-ttu-id="270b4-115">FolderUserFieldsAnsi: Deslocamento 0x0.</span><span class="sxs-lookup"><span data-stu-id="270b4-115">FolderUserFieldsAnsi: Offset 0x0.</span></span>
    
  - <span data-ttu-id="270b4-116">FieldDefinitionCount: Deslocamento 0x0, 4 bytes: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="270b4-116">FieldDefinitionCount: Offset 0x0, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="270b4-117">FieldDefinitions: Deslocamento 0x4, matriz de fluxos de FolderFieldDefinitionA 2.</span><span class="sxs-lookup"><span data-stu-id="270b4-117">FieldDefinitions: Offset 0x4, array of 2 FolderFieldDefinitionA streams.</span></span>
    
    <span data-ttu-id="270b4-118">O **primeiro elemento da matriz**:</span><span class="sxs-lookup"><span data-stu-id="270b4-118">**First array element**:</span></span>
    
    - <span data-ttu-id="270b4-119">FieldType: Deslocamento 0x4, 4 bytes: 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="270b4-119">FieldType: Offset 0x4, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="270b4-120">FieldNameLength: Deslocamento 0x8, 2 bytes: 0x000A (10)</span><span class="sxs-lookup"><span data-stu-id="270b4-120">FieldNameLength: Offset 0x8, 2 bytes: 0x000A (10)</span></span>
      
    - <span data-ttu-id="270b4-121">FieldName: Deslocamento 0xA, matriz de 10 caracteres.</span><span class="sxs-lookup"><span data-stu-id="270b4-121">FieldName: Offset 0xA, array of 10 CHARs.</span></span> <span data-ttu-id="270b4-122">Valor de cadeia de caracteres ANSI: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="270b4-122">ANSI string value: "TextField1".</span></span>
      
    - <span data-ttu-id="270b4-123">Comuns: Deslocamento 0x14.</span><span class="sxs-lookup"><span data-stu-id="270b4-123">Common: Offset 0x14.</span></span>
    
      - <span data-ttu-id="270b4-124">PropSetGuid: Deslocamento 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="270b4-124">PropSetGuid: Offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="270b4-125">fcapm: deslocamento 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="270b4-125">fcapm: Offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="270b4-126">dwString: Offset 0x28, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-126">dwString: Offset 0x28, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-127">dwBitmap: deslocamento 0x2C, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-127">dwBitmap: Offset 0x2C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-128">dwDisplay: deslocamento 0x30, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-128">dwDisplay: Offset 0x30, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-129">iFmt: deslocamento 0x34, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-129">iFmt: Offset 0x34, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-130">wszFormulaLength: deslocamento 0x38, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="270b4-130">wszFormulaLength: Offset 0x38, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="270b4-131">wszFormula: deslocamento 0x3A, matriz de WCHARs 0.</span><span class="sxs-lookup"><span data-stu-id="270b4-131">wszFormula: Offset 0x3A, array of 0 WCHARs.</span></span> <span data-ttu-id="270b4-132">Valor de cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="270b4-132">Empty string value.</span></span>
    
    <span data-ttu-id="270b4-133">O **segundo elemento de matriz**:</span><span class="sxs-lookup"><span data-stu-id="270b4-133">**Second array element**:</span></span>
    
    - <span data-ttu-id="270b4-134">FieldType: Deslocamento 0x3A, 4 bytes: 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="270b4-134">FieldType: Offset 0x3A, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="270b4-135">FieldNameLength: Deslocamento 0x3E, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="270b4-135">FieldNameLength: Offset 0x3E, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="270b4-136">FieldName: Deslocamento 0x40, matriz de caracteres de 0.</span><span class="sxs-lookup"><span data-stu-id="270b4-136">FieldName: Offset 0x40, array of 0 CHARs.</span></span> <span data-ttu-id="270b4-137">Valor de cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="270b4-137">Empty string value.</span></span>
      
    - <span data-ttu-id="270b4-138">Comuns: Deslocamento 0x40.</span><span class="sxs-lookup"><span data-stu-id="270b4-138">Common: Offset 0x40.</span></span>
    
      - <span data-ttu-id="270b4-139">PropSetGuid: Deslocamento 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="270b4-139">PropSetGuid: Offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="270b4-140">fcapm: deslocamento 0x50, 4 bytes: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="270b4-140">fcapm: Offset 0x50, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="270b4-141">dwString: deslocamento 0x54, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-141">dwString: Offset 0x54, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-142">dwBitmap: deslocamento 0x58, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-142">dwBitmap: Offset 0x58, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-143">dwDisplay: deslocamento 0x5C, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-143">dwDisplay: Offset 0x5C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-144">iFmt: deslocamento 0x60, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-144">iFmt: Offset 0x60, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-145">wszFormulaLength: deslocamento 0x64, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="270b4-145">wszFormulaLength: Offset 0x64, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="270b4-146">wszFormula: deslocamento 0x66, matriz de WCHARs 0.</span><span class="sxs-lookup"><span data-stu-id="270b4-146">wszFormula: Offset 0x66, array of 0 WCHARs.</span></span> <span data-ttu-id="270b4-147">Valor de cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="270b4-147">Empty string value.</span></span>
    
- <span data-ttu-id="270b4-148">FolderUserFieldsUnicode: Deslocamento 0x66.</span><span class="sxs-lookup"><span data-stu-id="270b4-148">FolderUserFieldsUnicode: Offset 0x66.</span></span>
    
  - <span data-ttu-id="270b4-149">FieldDefinitionCount: Deslocamento 0x66, 4 bytes: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="270b4-149">FieldDefinitionCount: Offset 0x66, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="270b4-150">FieldDefinitions: Deslocamento 0x6A, matriz de fluxos de FolderFieldDefinitionW 2.</span><span class="sxs-lookup"><span data-stu-id="270b4-150">FieldDefinitions: Offset 0x6A, array of 2 FolderFieldDefinitionW streams.</span></span>
    
    <span data-ttu-id="270b4-151">O **primeiro elemento da matriz**:</span><span class="sxs-lookup"><span data-stu-id="270b4-151">**First array element**:</span></span>
    
    - <span data-ttu-id="270b4-152">FieldType: Deslocamento 0x6A, 4 bytes: 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="270b4-152">FieldType: Offset 0x6A, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="270b4-153">FieldNameLength: Deslocamento 0x6E, 2 bytes: 0x000A (10).</span><span class="sxs-lookup"><span data-stu-id="270b4-153">FieldNameLength: Offset 0x6E, 2 bytes: 0x000A (10).</span></span>
      
    - <span data-ttu-id="270b4-154">FieldName: Deslocamento 0x70, matriz de 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="270b4-154">FieldName: Offset 0x70, array of 10 WCHARs.</span></span> <span data-ttu-id="270b4-155">Valor de cadeia de caracteres Unicode: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="270b4-155">Unicode string value: "TextField1".</span></span>
      
    - <span data-ttu-id="270b4-156">Comuns: Deslocamento 0x84.</span><span class="sxs-lookup"><span data-stu-id="270b4-156">Common: Offset 0x84.</span></span>
    
      - <span data-ttu-id="270b4-157">PropSetGuid: Deslocamento 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="270b4-157">PropSetGuid: Offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="270b4-158">fcapm: deslocamento 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="270b4-158">fcapm: Offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="270b4-159">dwString: deslocamento 0x98, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-159">dwString: Offset 0x98, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-160">dwBitmap: deslocamento 0x9C, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-160">dwBitmap: Offset 0x9C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-161">dwDisplay: deslocamento 0xA0, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-161">dwDisplay: Offset 0xA0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-162">iFmt: deslocamento 0xA4, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-162">iFmt: Offset 0xA4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-163">wszFormulaLength: deslocamento 0xA8, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="270b4-163">wszFormulaLength: Offset 0xA8, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="270b4-164">wszFormula: deslocamento 0xAA, matriz de WCHARs 0.</span><span class="sxs-lookup"><span data-stu-id="270b4-164">wszFormula: Offset 0xAA, array of 0 WCHARs.</span></span> <span data-ttu-id="270b4-165">Valor de cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="270b4-165">Empty string value.</span></span>
    
    <span data-ttu-id="270b4-166">O **segundo elemento de matriz**:</span><span class="sxs-lookup"><span data-stu-id="270b4-166">**Second array element**:</span></span>
    
    - <span data-ttu-id="270b4-167">FieldType: Deslocamento 0xAA, 4 bytes: 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="270b4-167">FieldType: Offset 0xAA, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="270b4-168">FieldNameLength: Deslocamento 0xAE, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="270b4-168">FieldNameLength: Offset 0xAE, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="270b4-169">FieldName: Deslocamento 0xB0, matriz de WCHARs 0.</span><span class="sxs-lookup"><span data-stu-id="270b4-169">FieldName: Offset 0xB0, array of 0 WCHARs.</span></span> <span data-ttu-id="270b4-170">Valor de cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="270b4-170">Empty string value.</span></span>
      
    - <span data-ttu-id="270b4-171">Comuns: Deslocamento 0xB0.</span><span class="sxs-lookup"><span data-stu-id="270b4-171">Common: Offset 0xB0.</span></span>
    
      - <span data-ttu-id="270b4-172">PropSetGuid: Deslocamento 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="270b4-172">PropSetGuid: Offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="270b4-173">fcapm: deslocamento 0xC0, 4 bytes: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="270b4-173">fcapm: Offset 0xC0, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="270b4-174">dwString: deslocamento 0xC4, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-174">dwString: Offset 0xC4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-175">dwBitmap: deslocamento 0xC8, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-175">dwBitmap: Offset 0xC8, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-176">dwDisplay: deslocamento 0xCC, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-176">dwDisplay: Offset 0xCC, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-177">iFmt: deslocamento 0xD0, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="270b4-177">iFmt: Offset 0xD0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="270b4-178">wszFormulaLength: deslocamento 0xD4, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="270b4-178">wszFormulaLength: Offset 0xD4, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="270b4-179">wszFormula: deslocamento 0xD6, matriz de WCHARs 0.</span><span class="sxs-lookup"><span data-stu-id="270b4-179">wszFormula: Offset 0xD6, array of 0 WCHARs.</span></span> <span data-ttu-id="270b4-180">Valor de cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="270b4-180">Empty string value.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="270b4-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="270b4-181">See also</span></span>

- [<span data-ttu-id="270b4-182">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="270b4-182">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="270b4-183">Estrutura de fluxo de PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="270b4-183">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="270b4-184">Estrutura de fluxo de FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="270b4-184">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="270b4-185">Estrutura de fluxo de SkipBlock</span><span class="sxs-lookup"><span data-stu-id="270b4-185">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="270b4-186">Estrutura de fluxo de FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="270b4-186">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="270b4-187">Estrutura de fluxo de PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="270b4-187">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="270b4-188">Estrutura de fluxo de PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="270b4-188">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

