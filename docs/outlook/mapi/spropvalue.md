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
# <a name="spropvalue"></a><span data-ttu-id="b158f-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b158f-103">SPropValue</span></span>

  
  
<span data-ttu-id="b158f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b158f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b158f-105">Descreve uma propriedade MAPI.</span><span class="sxs-lookup"><span data-stu-id="b158f-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b158f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b158f-106">Header file:</span></span>  <br/> |<span data-ttu-id="b158f-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b158f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b158f-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="b158f-108">Related macros:</span></span>  <br/> |<span data-ttu-id="b158f-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="b158f-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="b158f-110">Members</span><span class="sxs-lookup"><span data-stu-id="b158f-110">Members</span></span>

 <span data-ttu-id="b158f-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="b158f-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="b158f-112">Marca de propriedade da propriedade.</span><span class="sxs-lookup"><span data-stu-id="b158f-112">Property tag for the property.</span></span> <span data-ttu-id="b158f-113">As marcas de propriedade são inteiros não assinados de 32 bits que consistem no identificador exclusivo da propriedade nos 16 bits de ordem alta e no tipo da propriedade na ordem baixa de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b158f-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="b158f-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="b158f-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="b158f-115">Reservado para MAPI; Não use.</span><span class="sxs-lookup"><span data-stu-id="b158f-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="b158f-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b158f-116">**Value**</span></span>
  
> <span data-ttu-id="b158f-117">União de valores de dados, o valor específico determinado pelo tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b158f-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="b158f-118">A tabela a seguir lista para cada tipo de propriedade, o membro da União que deve ser usado e seu tipo de dados associado.</span><span class="sxs-lookup"><span data-stu-id="b158f-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="b158f-119">**Tipo de propriedade**</span><span class="sxs-lookup"><span data-stu-id="b158f-119">**Property type**</span></span>|<span data-ttu-id="b158f-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b158f-120">**Value**</span></span>|<span data-ttu-id="b158f-121">**Tipo de dados do valor**</span><span class="sxs-lookup"><span data-stu-id="b158f-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b158f-122">PT_I2 ou PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="b158f-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="b158f-123">**i**</span><span class="sxs-lookup"><span data-stu-id="b158f-123">**i**</span></span> <br/> |<span data-ttu-id="b158f-124">short int</span><span class="sxs-lookup"><span data-stu-id="b158f-124">short int</span></span>  <br/> |
|<span data-ttu-id="b158f-125">PT_I4 ou PT_LONG (assinado)</span><span class="sxs-lookup"><span data-stu-id="b158f-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="b158f-126">**Esq**</span><span class="sxs-lookup"><span data-stu-id="b158f-126">**l**</span></span> <br/> |<span data-ttu-id="b158f-127">Longas</span><span class="sxs-lookup"><span data-stu-id="b158f-127">LONG</span></span>  <br/> |
|<span data-ttu-id="b158f-128">PT_I4 ou PT_LONG (não assinado)</span><span class="sxs-lookup"><span data-stu-id="b158f-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="b158f-129">**UL**</span><span class="sxs-lookup"><span data-stu-id="b158f-129">**ul**</span></span> <br/> |<span data-ttu-id="b158f-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="b158f-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="b158f-131">PT_R4 ou PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="b158f-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="b158f-132">**FLT**</span><span class="sxs-lookup"><span data-stu-id="b158f-132">**flt**</span></span> <br/> |<span data-ttu-id="b158f-133">float</span><span class="sxs-lookup"><span data-stu-id="b158f-133">float</span></span>  <br/> |
|<span data-ttu-id="b158f-134">PT_R8 ou PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="b158f-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="b158f-135">**ao duas vezes**</span><span class="sxs-lookup"><span data-stu-id="b158f-135">**dbl**</span></span> <br/> |<span data-ttu-id="b158f-136">double</span><span class="sxs-lookup"><span data-stu-id="b158f-136">double</span></span>  <br/> |
|<span data-ttu-id="b158f-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b158f-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="b158f-138">**b**</span><span class="sxs-lookup"><span data-stu-id="b158f-138">**b**</span></span> <br/> |<span data-ttu-id="b158f-139">int curto não assinado</span><span class="sxs-lookup"><span data-stu-id="b158f-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="b158f-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="b158f-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="b158f-141">**cur**</span><span class="sxs-lookup"><span data-stu-id="b158f-141">**cur**</span></span> <br/> |[<span data-ttu-id="b158f-142">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="b158f-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="b158f-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="b158f-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="b158f-144">**por**</span><span class="sxs-lookup"><span data-stu-id="b158f-144">**at**</span></span> <br/> |<span data-ttu-id="b158f-145">double</span><span class="sxs-lookup"><span data-stu-id="b158f-145">double</span></span>  <br/> |
|<span data-ttu-id="b158f-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b158f-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="b158f-147">**ft**</span><span class="sxs-lookup"><span data-stu-id="b158f-147">**ft**</span></span> <br/> |[<span data-ttu-id="b158f-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="b158f-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="b158f-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="b158f-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="b158f-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="b158f-150">**lpszA**</span></span> <br/> |<span data-ttu-id="b158f-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="b158f-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="b158f-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b158f-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="b158f-153">**Bno**</span><span class="sxs-lookup"><span data-stu-id="b158f-153">**bin**</span></span> <br/> |<span data-ttu-id="b158f-154">BYTE [matriz]</span><span class="sxs-lookup"><span data-stu-id="b158f-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="b158f-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b158f-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="b158f-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="b158f-156">**lpszW**</span></span> <br/> |<span data-ttu-id="b158f-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="b158f-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="b158f-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="b158f-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="b158f-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="b158f-159">**lpguid**</span></span> <br/> |<span data-ttu-id="b158f-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="b158f-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="b158f-161">PT_I8 ou PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="b158f-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="b158f-162">**Li**</span><span class="sxs-lookup"><span data-stu-id="b158f-162">**li**</span></span> <br/> |<span data-ttu-id="b158f-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="b158f-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="b158f-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="b158f-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="b158f-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="b158f-165">**MVi**</span></span> <br/> |[<span data-ttu-id="b158f-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="b158f-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="b158f-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="b158f-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="b158f-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="b158f-168">**MVI**</span></span> <br/> |[<span data-ttu-id="b158f-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="b158f-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="b158f-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="b158f-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="b158f-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="b158f-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="b158f-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="b158f-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="b158f-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="b158f-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="b158f-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="b158f-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="b158f-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="b158f-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="b158f-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="b158f-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="b158f-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="b158f-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="b158f-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="b158f-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="b158f-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="b158f-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="b158f-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="b158f-180">**MVat**</span></span> <br/> |[<span data-ttu-id="b158f-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="b158f-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="b158f-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b158f-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="b158f-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="b158f-183">**MVft**</span></span> <br/> |[<span data-ttu-id="b158f-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="b158f-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="b158f-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="b158f-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="b158f-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="b158f-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="b158f-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="b158f-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="b158f-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="b158f-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="b158f-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="b158f-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="b158f-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="b158f-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="b158f-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b158f-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="b158f-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="b158f-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="b158f-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="b158f-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="b158f-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="b158f-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="b158f-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="b158f-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="b158f-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="b158f-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="b158f-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="b158f-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="b158f-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="b158f-198">**MVli**</span></span> <br/> |[<span data-ttu-id="b158f-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="b158f-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="b158f-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="b158f-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="b158f-201">**err**</span><span class="sxs-lookup"><span data-stu-id="b158f-201">**err**</span></span> <br/> |[<span data-ttu-id="b158f-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="b158f-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="b158f-203">PT_NULL ou PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="b158f-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="b158f-204">**x**</span><span class="sxs-lookup"><span data-stu-id="b158f-204">**x**</span></span> <br/> |<span data-ttu-id="b158f-205">Longas</span><span class="sxs-lookup"><span data-stu-id="b158f-205">LONG</span></span>  <br/> |
|<span data-ttu-id="b158f-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="b158f-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="b158f-207">**LPV**</span><span class="sxs-lookup"><span data-stu-id="b158f-207">**lpv**</span></span> <br/> |<span data-ttu-id="b158f-208">Deixa\*</span><span class="sxs-lookup"><span data-stu-id="b158f-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b158f-209">Comentários</span><span class="sxs-lookup"><span data-stu-id="b158f-209">Remarks</span></span>

<span data-ttu-id="b158f-210">O membro **ulPropTag** é composto de duas partes:</span><span class="sxs-lookup"><span data-stu-id="b158f-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="b158f-211">Um identificador na ordem alta de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b158f-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="b158f-212">Um tipo na ordem baixa de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b158f-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="b158f-213">O identificador é um valor numérico dentro de um determinado intervalo.</span><span class="sxs-lookup"><span data-stu-id="b158f-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="b158f-214">MAPI define intervalos para identificadores para descrever o que a propriedade é usada e quem é responsável por mantê-la.</span><span class="sxs-lookup"><span data-stu-id="b158f-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="b158f-215">MAPI define restrições para cada uma das marcas de propriedade que ele suporta no arquivo de cabeçalho Mapitags. h.</span><span class="sxs-lookup"><span data-stu-id="b158f-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="b158f-216">O tipo indica o formato do valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="b158f-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="b158f-217">MAPI define constantes para cada um dos tipos de propriedade que ele suporta no arquivo de cabeçalho mapidefs. h.</span><span class="sxs-lookup"><span data-stu-id="b158f-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="b158f-218">Para obter uma lista completa dos intervalos de propriedades válidos para identificadores e tipos de propriedade, consulte o apêndice de [identificadores e tipos](property-identifiers-and-types.md) de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b158f-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="b158f-219">O membro **dwAlignPad** é usado como preenchimento para garantir o alinhamento correto nos computadores que exigem o alinhamento de 8 bytes para valores de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="b158f-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="b158f-220">Os desenvolvedores que escrevem código nesses computadores devem usar rotinas de alocação de memória que alocam os arrays do **SPropValue** em limites de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="b158f-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="b158f-221">Para obter mais informações, consulte [MAPI Property Type Overview](mapi-property-type-overview.md) e [atualizating MAPI Properties](updating-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="b158f-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b158f-222">Confira também</span><span class="sxs-lookup"><span data-stu-id="b158f-222">See also</span></span>



[<span data-ttu-id="b158f-223">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="b158f-223">MAPI Structures</span></span>](mapi-structures.md)

