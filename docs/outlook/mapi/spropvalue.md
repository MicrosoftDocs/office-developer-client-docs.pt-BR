---
title: SPropValue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropValue
api_type:
- COM
ms.assetid: faf795a2-84db-432d-a05f-082f25a5cab5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c7f4e8835831af6277cef134bf3961e9928cba33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433525"
---
# <a name="spropvalue"></a><span data-ttu-id="756ee-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="756ee-103">SPropValue</span></span>

  
  
<span data-ttu-id="756ee-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="756ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="756ee-105">Descreve uma propriedade MAPI.</span><span class="sxs-lookup"><span data-stu-id="756ee-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="756ee-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="756ee-106">Header file:</span></span>  <br/> |<span data-ttu-id="756ee-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="756ee-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="756ee-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="756ee-108">Related macros:</span></span>  <br/> |<span data-ttu-id="756ee-109">[CHANGE_PROP_TYPE,](change_prop_type.md) [MVI_PROP,](mvi_prop.md) [PROP_ID,](prop_id.md) [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="756ee-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="756ee-110">Members</span><span class="sxs-lookup"><span data-stu-id="756ee-110">Members</span></span>

 <span data-ttu-id="756ee-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="756ee-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="756ee-112">Marca de propriedade da propriedade.</span><span class="sxs-lookup"><span data-stu-id="756ee-112">Property tag for the property.</span></span> <span data-ttu-id="756ee-113">As marcas de propriedade são inteiros não assinados de 32 bits que consistem no identificador exclusivo da propriedade nos 16 bits de ordem alta e no tipo da propriedade nos 16 bits de ordem baixa.</span><span class="sxs-lookup"><span data-stu-id="756ee-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="756ee-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="756ee-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="756ee-115">Reservado para MAPI; não usar.</span><span class="sxs-lookup"><span data-stu-id="756ee-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="756ee-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="756ee-116">**Value**</span></span>
  
> <span data-ttu-id="756ee-117">União de valores de dados, o valor específico ditado pelo tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="756ee-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="756ee-118">A tabela a seguir lista para cada tipo de propriedade, o membro da união que deve ser usado e seu tipo de dados associado.</span><span class="sxs-lookup"><span data-stu-id="756ee-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="756ee-119">**Tipo de propriedade**</span><span class="sxs-lookup"><span data-stu-id="756ee-119">**Property type**</span></span>|<span data-ttu-id="756ee-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="756ee-120">**Value**</span></span>|<span data-ttu-id="756ee-121">**Tipo de dados de Valor**</span><span class="sxs-lookup"><span data-stu-id="756ee-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="756ee-122">PT_I2 ou PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="756ee-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="756ee-123">**i**</span><span class="sxs-lookup"><span data-stu-id="756ee-123">**i**</span></span> <br/> |<span data-ttu-id="756ee-124">short int</span><span class="sxs-lookup"><span data-stu-id="756ee-124">short int</span></span>  <br/> |
|<span data-ttu-id="756ee-125">PT_I4 ou PT_LONG (assinado)</span><span class="sxs-lookup"><span data-stu-id="756ee-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="756ee-126">**l**</span><span class="sxs-lookup"><span data-stu-id="756ee-126">**l**</span></span> <br/> |<span data-ttu-id="756ee-127">LONG</span><span class="sxs-lookup"><span data-stu-id="756ee-127">LONG</span></span>  <br/> |
|<span data-ttu-id="756ee-128">PT_I4 ou PT_LONG (não assinado)</span><span class="sxs-lookup"><span data-stu-id="756ee-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="756ee-129">**ul**</span><span class="sxs-lookup"><span data-stu-id="756ee-129">**ul**</span></span> <br/> |<span data-ttu-id="756ee-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="756ee-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="756ee-131">PT_R4 ou PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="756ee-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="756ee-132">**flt**</span><span class="sxs-lookup"><span data-stu-id="756ee-132">**flt**</span></span> <br/> |<span data-ttu-id="756ee-133">flutuação</span><span class="sxs-lookup"><span data-stu-id="756ee-133">float</span></span>  <br/> |
|<span data-ttu-id="756ee-134">PT_R8 ou PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="756ee-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="756ee-135">**dbl**</span><span class="sxs-lookup"><span data-stu-id="756ee-135">**dbl**</span></span> <br/> |<span data-ttu-id="756ee-136">double</span><span class="sxs-lookup"><span data-stu-id="756ee-136">double</span></span>  <br/> |
|<span data-ttu-id="756ee-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="756ee-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="756ee-138">**b**</span><span class="sxs-lookup"><span data-stu-id="756ee-138">**b**</span></span> <br/> |<span data-ttu-id="756ee-139">unsigned short int</span><span class="sxs-lookup"><span data-stu-id="756ee-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="756ee-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="756ee-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="756ee-141">**cur**</span><span class="sxs-lookup"><span data-stu-id="756ee-141">**cur**</span></span> <br/> |[<span data-ttu-id="756ee-142">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="756ee-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="756ee-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="756ee-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="756ee-144">**em**</span><span class="sxs-lookup"><span data-stu-id="756ee-144">**at**</span></span> <br/> |<span data-ttu-id="756ee-145">double</span><span class="sxs-lookup"><span data-stu-id="756ee-145">double</span></span>  <br/> |
|<span data-ttu-id="756ee-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="756ee-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="756ee-147">**ft**</span><span class="sxs-lookup"><span data-stu-id="756ee-147">**ft**</span></span> <br/> |[<span data-ttu-id="756ee-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="756ee-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="756ee-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="756ee-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="756ee-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="756ee-150">**lpszA**</span></span> <br/> |<span data-ttu-id="756ee-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="756ee-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="756ee-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="756ee-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="756ee-153">**bin**</span><span class="sxs-lookup"><span data-stu-id="756ee-153">**bin**</span></span> <br/> |<span data-ttu-id="756ee-154">BYTE [matriz]</span><span class="sxs-lookup"><span data-stu-id="756ee-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="756ee-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="756ee-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="756ee-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="756ee-156">**lpszW**</span></span> <br/> |<span data-ttu-id="756ee-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="756ee-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="756ee-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="756ee-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="756ee-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="756ee-159">**lpguid**</span></span> <br/> |<span data-ttu-id="756ee-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="756ee-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="756ee-161">PT_I8 ou PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="756ee-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="756ee-162">**li**</span><span class="sxs-lookup"><span data-stu-id="756ee-162">**li**</span></span> <br/> |<span data-ttu-id="756ee-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="756ee-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="756ee-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="756ee-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="756ee-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="756ee-165">**MVi**</span></span> <br/> |[<span data-ttu-id="756ee-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="756ee-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="756ee-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="756ee-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="756ee-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="756ee-168">**MVI**</span></span> <br/> |[<span data-ttu-id="756ee-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="756ee-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="756ee-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="756ee-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="756ee-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="756ee-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="756ee-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="756ee-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="756ee-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="756ee-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="756ee-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="756ee-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="756ee-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="756ee-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="756ee-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="756ee-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="756ee-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="756ee-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="756ee-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="756ee-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="756ee-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="756ee-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="756ee-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="756ee-180">**MVat**</span></span> <br/> |[<span data-ttu-id="756ee-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="756ee-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="756ee-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="756ee-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="756ee-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="756ee-183">**MVft**</span></span> <br/> |[<span data-ttu-id="756ee-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="756ee-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="756ee-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="756ee-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="756ee-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="756ee-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="756ee-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="756ee-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="756ee-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="756ee-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="756ee-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="756ee-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="756ee-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="756ee-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="756ee-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="756ee-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="756ee-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="756ee-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="756ee-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="756ee-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="756ee-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="756ee-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="756ee-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="756ee-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="756ee-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="756ee-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="756ee-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="756ee-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="756ee-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="756ee-198">**MVli**</span></span> <br/> |[<span data-ttu-id="756ee-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="756ee-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="756ee-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="756ee-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="756ee-201">**err**</span><span class="sxs-lookup"><span data-stu-id="756ee-201">**err**</span></span> <br/> |[<span data-ttu-id="756ee-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="756ee-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="756ee-203">PT_NULL ou PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="756ee-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="756ee-204">**x**</span><span class="sxs-lookup"><span data-stu-id="756ee-204">**x**</span></span> <br/> |<span data-ttu-id="756ee-205">LONG</span><span class="sxs-lookup"><span data-stu-id="756ee-205">LONG</span></span>  <br/> |
|<span data-ttu-id="756ee-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="756ee-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="756ee-207">**lpv**</span><span class="sxs-lookup"><span data-stu-id="756ee-207">**lpv**</span></span> <br/> |<span data-ttu-id="756ee-208">VOID \*</span><span class="sxs-lookup"><span data-stu-id="756ee-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="756ee-209">Comentários</span><span class="sxs-lookup"><span data-stu-id="756ee-209">Remarks</span></span>

<span data-ttu-id="756ee-210">O **membro ulPropTag** é feito de duas partes:</span><span class="sxs-lookup"><span data-stu-id="756ee-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="756ee-211">Um identificador nos 16 bits de alta ordem.</span><span class="sxs-lookup"><span data-stu-id="756ee-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="756ee-212">Um tipo nos 16 bits de ordem baixa.</span><span class="sxs-lookup"><span data-stu-id="756ee-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="756ee-213">O identificador é um valor numérico dentro de um intervalo específico.</span><span class="sxs-lookup"><span data-stu-id="756ee-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="756ee-214">O MAPI define intervalos para que os identificadores descrevam para que a propriedade é usada e para quem é responsável por mantê-la.</span><span class="sxs-lookup"><span data-stu-id="756ee-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="756ee-215">MAPI define restrições para cada uma das marcas de propriedade que ele suporta no arquivo de título Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="756ee-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="756ee-216">O tipo indica o formato do valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="756ee-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="756ee-217">MAPI define constantes para cada um dos tipos de propriedade que ele suporta no arquivo de header Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="756ee-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="756ee-218">Para uma lista completa dos intervalos de propriedades válidos para identificadores e tipos de propriedade, consulte o apêndice [Identificadores](property-identifiers-and-types.md) e Tipos de Propriedade.</span><span class="sxs-lookup"><span data-stu-id="756ee-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="756ee-219">O **membro dwAlignPad** é usado como preenchimento para garantir o alinhamento adequado em computadores que exigem alinhamento de 8 byte para valores de 8 byte.</span><span class="sxs-lookup"><span data-stu-id="756ee-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="756ee-220">Os desenvolvedores que escrevem código nesses computadores devem usar rotinas de alocação de memória que alocam as matrizes **SPropValue** em limites de 8 byte.</span><span class="sxs-lookup"><span data-stu-id="756ee-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="756ee-221">Para obter mais informações, consulte [Visão geral do tipo de propriedade MAPI](mapi-property-type-overview.md) e atualização de propriedades [MAPI](updating-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="756ee-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="756ee-222">Confira também</span><span class="sxs-lookup"><span data-stu-id="756ee-222">See also</span></span>



[<span data-ttu-id="756ee-223">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="756ee-223">MAPI Structures</span></span>](mapi-structures.md)

