---
title: Exemplo de fluxo FolderUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e5251a619c70221987847830897ba349d63fd9cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433973"
---
# <a name="folderuserfields-stream-sample"></a><span data-ttu-id="5f9b8-103">Exemplo de fluxo FolderUserFields</span><span class="sxs-lookup"><span data-stu-id="5f9b8-103">FolderUserFields stream sample</span></span>

<span data-ttu-id="5f9b8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f9b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f9b8-105">Este tópico descreve um exemplo de um fluxo do FolderUserFields.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-105">This topic describes an example of a FolderUserFields stream.</span></span> <span data-ttu-id="5f9b8-106">O Stream contém uma definição de um campo definido pelo usuário `TextField1`.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="5f9b8-107">O tipo é **Text**e o Stream FolderUserFields contém as partes FolderUserFieldsAnsi e FolderUserFieldsUnicode.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-107">The type is **Text**, and the FolderUserFields stream contains both FolderUserFieldsAnsi and FolderUserFieldsUnicode parts.</span></span> <span data-ttu-id="5f9b8-108">Para obter mais informações, consulte [estruturas de fluxo de campos de pasta](folder-fields-stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-108">For more information see [Folder Fields Stream Structures](folder-fields-stream-structures.md).</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="5f9b8-109">Despejo de dados</span><span class="sxs-lookup"><span data-stu-id="5f9b8-109">Data dump</span></span>

<span data-ttu-id="5f9b8-110">O seguinte é um despejo de dados do Stream como seria exibido em um editor binário.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-110">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="5f9b8-111">Deslocamento de fluxo</span><span class="sxs-lookup"><span data-stu-id="5f9b8-111">Stream offset</span></span>|<span data-ttu-id="5f9b8-112">Bytes de dados</span><span class="sxs-lookup"><span data-stu-id="5f9b8-112">Data bytes</span></span>|<span data-ttu-id="5f9b8-113">Dados ASCII</span><span class="sxs-lookup"><span data-stu-id="5f9b8-113">ASCII data</span></span>|
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
   

<span data-ttu-id="5f9b8-114">Veja a seguir uma análise dos dados de exemplo para o fluxo **FolderUserFields** :</span><span class="sxs-lookup"><span data-stu-id="5f9b8-114">The following is a parse of the sample data for the **FolderUserFields** stream:</span></span>
  
- <span data-ttu-id="5f9b8-115">FolderUserFieldsAnsi: offset 0x0.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-115">FolderUserFieldsAnsi: Offset 0x0.</span></span>
    
  - <span data-ttu-id="5f9b8-116">FieldDefinitionCount: offset 0x0, 4 bytes: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-116">FieldDefinitionCount: Offset 0x0, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="5f9b8-117">FieldDefinitions: offset 0x4, matriz de 2 fluxos de FolderFieldDefinitionA.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-117">FieldDefinitions: Offset 0x4, array of 2 FolderFieldDefinitionA streams.</span></span>
    
    <span data-ttu-id="5f9b8-118">**Primeiro elemento de matriz**:</span><span class="sxs-lookup"><span data-stu-id="5f9b8-118">**First array element**:</span></span>
    
    - <span data-ttu-id="5f9b8-119">FieldType: offset 0x4, 4 bytes: 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-119">FieldType: Offset 0x4, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="5f9b8-120">FieldNameLength: offset 0x8, 2 bytes: 0x000A (10)</span><span class="sxs-lookup"><span data-stu-id="5f9b8-120">FieldNameLength: Offset 0x8, 2 bytes: 0x000A (10)</span></span>
      
    - <span data-ttu-id="5f9b8-121">FieldName: offset 0xA, matriz de 10 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-121">FieldName: Offset 0xA, array of 10 CHARs.</span></span> <span data-ttu-id="5f9b8-122">Valor da cadeia de caracteres ANSI: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-122">ANSI string value: "TextField1".</span></span>
      
    - <span data-ttu-id="5f9b8-123">Comum: offset 0x14.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-123">Common: Offset 0x14.</span></span>
    
      - <span data-ttu-id="5f9b8-124">PropSetGuid: offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-124">PropSetGuid: Offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="5f9b8-125">fcapm: offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-125">fcapm: Offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="5f9b8-126">dwString: offset 0x28, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-126">dwString: Offset 0x28, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-127">dwBitmap: offset 0x2C, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-127">dwBitmap: Offset 0x2C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-128">dwDisplay: offset 0x30, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-128">dwDisplay: Offset 0x30, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-129">iFmt: offset 0x34, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-129">iFmt: Offset 0x34, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-130">wszFormulaLength: offset 0x38, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-130">wszFormulaLength: Offset 0x38, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="5f9b8-131">wszFormula: offset 0x3A, matriz de 0 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-131">wszFormula: Offset 0x3A, array of 0 WCHARs.</span></span> <span data-ttu-id="5f9b8-132">Valor de cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-132">Empty string value.</span></span>
    
    <span data-ttu-id="5f9b8-133">**Segundo elemento de matriz**:</span><span class="sxs-lookup"><span data-stu-id="5f9b8-133">**Second array element**:</span></span>
    
    - <span data-ttu-id="5f9b8-134">FieldType: offset 0x3A, 4 bytes: 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-134">FieldType: Offset 0x3A, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="5f9b8-135">FieldNameLength: offset 0x3E, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-135">FieldNameLength: Offset 0x3E, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="5f9b8-136">FieldName: offset 0x40, matriz de 0 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-136">FieldName: Offset 0x40, array of 0 CHARs.</span></span> <span data-ttu-id="5f9b8-137">Valor de cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-137">Empty string value.</span></span>
      
    - <span data-ttu-id="5f9b8-138">Comum: offset 0x40.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-138">Common: Offset 0x40.</span></span>
    
      - <span data-ttu-id="5f9b8-139">PropSetGuid: offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-139">PropSetGuid: Offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="5f9b8-140">fcapm: offset 0x50, 4 bytes: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-140">fcapm: Offset 0x50, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="5f9b8-141">dwString: offset 0x54, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-141">dwString: Offset 0x54, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-142">dwBitmap: offset 0x58, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-142">dwBitmap: Offset 0x58, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-143">dwDisplay: offset 0x5C, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-143">dwDisplay: Offset 0x5C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-144">iFmt: offset 0x60, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-144">iFmt: Offset 0x60, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-145">wszFormulaLength: offset 0x64, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-145">wszFormulaLength: Offset 0x64, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="5f9b8-146">wszFormula: offset 0x66, matriz de 0 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-146">wszFormula: Offset 0x66, array of 0 WCHARs.</span></span> <span data-ttu-id="5f9b8-147">Valor de cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-147">Empty string value.</span></span>
    
- <span data-ttu-id="5f9b8-148">FolderUserFieldsUnicode: offset 0x66.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-148">FolderUserFieldsUnicode: Offset 0x66.</span></span>
    
  - <span data-ttu-id="5f9b8-149">FieldDefinitionCount: offset 0x66, 4 bytes: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-149">FieldDefinitionCount: Offset 0x66, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="5f9b8-150">FieldDefinitions: offset 0x6A, matriz de 2 FolderFieldDefinitionW Streams.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-150">FieldDefinitions: Offset 0x6A, array of 2 FolderFieldDefinitionW streams.</span></span>
    
    <span data-ttu-id="5f9b8-151">**Primeiro elemento de matriz**:</span><span class="sxs-lookup"><span data-stu-id="5f9b8-151">**First array element**:</span></span>
    
    - <span data-ttu-id="5f9b8-152">FieldType: offset 0x6A, 4 bytes: 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-152">FieldType: Offset 0x6A, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="5f9b8-153">FieldNameLength: offset 0x6E, 2 bytes: 0x000A (10).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-153">FieldNameLength: Offset 0x6E, 2 bytes: 0x000A (10).</span></span>
      
    - <span data-ttu-id="5f9b8-154">FieldName: offset 0x70, matriz de 10 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-154">FieldName: Offset 0x70, array of 10 WCHARs.</span></span> <span data-ttu-id="5f9b8-155">Valor da cadeia de caracteres Unicode: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="5f9b8-155">Unicode string value: "TextField1".</span></span>
      
    - <span data-ttu-id="5f9b8-156">Comum: offset 0x84.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-156">Common: Offset 0x84.</span></span>
    
      - <span data-ttu-id="5f9b8-157">PropSetGuid: offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-157">PropSetGuid: Offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="5f9b8-158">fcapm: offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-158">fcapm: Offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="5f9b8-159">dwString: offset 0x98, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-159">dwString: Offset 0x98, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-160">dwBitmap: offset 0x9C, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-160">dwBitmap: Offset 0x9C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-161">dwDisplay: offset 0xA0, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-161">dwDisplay: Offset 0xA0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-162">iFmt: offset 0xA4, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-162">iFmt: Offset 0xA4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-163">wszFormulaLength: offset 0xA8, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-163">wszFormulaLength: Offset 0xA8, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="5f9b8-164">wszFormula: offset 0xAA, matriz de 0 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-164">wszFormula: Offset 0xAA, array of 0 WCHARs.</span></span> <span data-ttu-id="5f9b8-165">Valor de cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-165">Empty string value.</span></span>
    
    <span data-ttu-id="5f9b8-166">**Segundo elemento de matriz**:</span><span class="sxs-lookup"><span data-stu-id="5f9b8-166">**Second array element**:</span></span>
    
    - <span data-ttu-id="5f9b8-167">FieldType: offset 0xAA, 4 bytes: 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-167">FieldType: Offset 0xAA, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="5f9b8-168">FieldNameLength: offset 0xAE, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-168">FieldNameLength: Offset 0xAE, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="5f9b8-169">FieldName: offset 0xB0, matriz de 0 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-169">FieldName: Offset 0xB0, array of 0 WCHARs.</span></span> <span data-ttu-id="5f9b8-170">Valor de cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-170">Empty string value.</span></span>
      
    - <span data-ttu-id="5f9b8-171">Comum: offset 0xB0.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-171">Common: Offset 0xB0.</span></span>
    
      - <span data-ttu-id="5f9b8-172">PropSetGuid: offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-172">PropSetGuid: Offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="5f9b8-173">fcapm: offset 0xC0, 4 bytes: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-173">fcapm: Offset 0xC0, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="5f9b8-174">dwString: offset 0xC4, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-174">dwString: Offset 0xC4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-175">dwBitmap: offset 0xC8, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-175">dwBitmap: Offset 0xC8, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-176">dwDisplay: offset 0xCC, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-176">dwDisplay: Offset 0xCC, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-177">iFmt: offset 0xD0, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-177">iFmt: Offset 0xD0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="5f9b8-178">wszFormulaLength: offset 0xD4, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="5f9b8-178">wszFormulaLength: Offset 0xD4, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="5f9b8-179">wszFormula: offset 0xD6, matriz de 0 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-179">wszFormula: Offset 0xD6, array of 0 WCHARs.</span></span> <span data-ttu-id="5f9b8-180">Valor de cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="5f9b8-180">Empty string value.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f9b8-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f9b8-181">See also</span></span>

- [<span data-ttu-id="5f9b8-182">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="5f9b8-182">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="5f9b8-183">Estrutura de fluxo PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="5f9b8-183">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="5f9b8-184">Estrutura de fluxo FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="5f9b8-184">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="5f9b8-185">Estrutura de fluxo SkipBlock</span><span class="sxs-lookup"><span data-stu-id="5f9b8-185">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="5f9b8-186">Estrutura de fluxo FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="5f9b8-186">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="5f9b8-187">Estrutura de fluxo PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="5f9b8-187">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="5f9b8-188">Estrutura de fluxo PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="5f9b8-188">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

