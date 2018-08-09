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
ms.openlocfilehash: f378bdd473410b846328cbe1f911eba9401f88cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770495"
---
# <a name="spropvalue"></a><span data-ttu-id="550e3-103">SPropValue</span><span class="sxs-lookup"><span data-stu-id="550e3-103">SPropValue</span></span>

  
  
<span data-ttu-id="550e3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="550e3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="550e3-105">Descreve uma propriedade MAPI.</span><span class="sxs-lookup"><span data-stu-id="550e3-105">Describes a MAPI property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="550e3-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="550e3-106">Header file:</span></span>  <br/> |<span data-ttu-id="550e3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="550e3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="550e3-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="550e3-108">Related macros:</span></span>  <br/> |<span data-ttu-id="550e3-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span><span class="sxs-lookup"><span data-stu-id="550e3-109">[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a><span data-ttu-id="550e3-110">Members</span><span class="sxs-lookup"><span data-stu-id="550e3-110">Members</span></span>

 <span data-ttu-id="550e3-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="550e3-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="550e3-112">Marca de propriedade para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="550e3-112">Property tag for the property.</span></span> <span data-ttu-id="550e3-113">As marcas de propriedade são números inteiros não assinados de 32 bits consistindo a identificador exclusivo da propriedade nos 16 bits superiores e o tipo da propriedade nos ordem baixa 16 bits.</span><span class="sxs-lookup"><span data-stu-id="550e3-113">Property tags are 32-bit unsigned integers consisting of the property's unique identifier in the high-order 16 bits and the property's type in the low-order 16 bits.</span></span>
    
 <span data-ttu-id="550e3-114">**dwAlignPad**</span><span class="sxs-lookup"><span data-stu-id="550e3-114">**dwAlignPad**</span></span>
  
> <span data-ttu-id="550e3-115">Reservado para MAPI; Não use.</span><span class="sxs-lookup"><span data-stu-id="550e3-115">Reserved for MAPI; do not use.</span></span> 
    
 <span data-ttu-id="550e3-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="550e3-116">**Value**</span></span>
  
> <span data-ttu-id="550e3-117">União de valores de dados, o valor específico determinado pelo tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="550e3-117">Union of data values, the specific value dictated by the property type.</span></span> <span data-ttu-id="550e3-118">A tabela a seguir lista para cada tipo de propriedade, o membro da união que deverão ser usada e seu tipo de dados associados.</span><span class="sxs-lookup"><span data-stu-id="550e3-118">The following table lists for each property type, the member of the union that should be used and its associated data type.</span></span>
    
|<span data-ttu-id="550e3-119">**Tipo de propriedade**</span><span class="sxs-lookup"><span data-stu-id="550e3-119">**Property type**</span></span>|<span data-ttu-id="550e3-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="550e3-120">**Value**</span></span>|<span data-ttu-id="550e3-121">**Tipo de dados de valor**</span><span class="sxs-lookup"><span data-stu-id="550e3-121">**Data type of Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="550e3-122">PT_I2 ou PT_SHORT</span><span class="sxs-lookup"><span data-stu-id="550e3-122">PT_I2 or PT_SHORT</span></span>  <br/> |<span data-ttu-id="550e3-123">**Eu**</span><span class="sxs-lookup"><span data-stu-id="550e3-123">**i**</span></span> <br/> |<span data-ttu-id="550e3-124">short int</span><span class="sxs-lookup"><span data-stu-id="550e3-124">short int</span></span>  <br/> |
|<span data-ttu-id="550e3-125">PT_I4 ou PT_LONG (conectado)</span><span class="sxs-lookup"><span data-stu-id="550e3-125">PT_I4 or PT_LONG (signed)</span></span>  <br/> |<span data-ttu-id="550e3-126">**l**</span><span class="sxs-lookup"><span data-stu-id="550e3-126">**l**</span></span> <br/> |<span data-ttu-id="550e3-127">Longas</span><span class="sxs-lookup"><span data-stu-id="550e3-127">LONG</span></span>  <br/> |
|<span data-ttu-id="550e3-128">PT_I4 ou PT_LONG (sem sinal)</span><span class="sxs-lookup"><span data-stu-id="550e3-128">PT_I4 or PT_LONG (unsigned)</span></span>  <br/> |<span data-ttu-id="550e3-129">**UL**</span><span class="sxs-lookup"><span data-stu-id="550e3-129">**ul**</span></span> <br/> |<span data-ttu-id="550e3-130">ULONG</span><span class="sxs-lookup"><span data-stu-id="550e3-130">ULONG</span></span>  <br/> |
|<span data-ttu-id="550e3-131">PT_R4 ou PT_FLOAT</span><span class="sxs-lookup"><span data-stu-id="550e3-131">PT_R4 or PT_FLOAT</span></span>  <br/> |<span data-ttu-id="550e3-132">**especificados devem receber**</span><span class="sxs-lookup"><span data-stu-id="550e3-132">**flt**</span></span> <br/> |<span data-ttu-id="550e3-133">float</span><span class="sxs-lookup"><span data-stu-id="550e3-133">float</span></span>  <br/> |
|<span data-ttu-id="550e3-134">PT_R8 ou PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="550e3-134">PT_R8 or PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="550e3-135">**duplo**</span><span class="sxs-lookup"><span data-stu-id="550e3-135">**dbl**</span></span> <br/> |<span data-ttu-id="550e3-136">double</span><span class="sxs-lookup"><span data-stu-id="550e3-136">double</span></span>  <br/> |
|<span data-ttu-id="550e3-137">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="550e3-137">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="550e3-138">**b**</span><span class="sxs-lookup"><span data-stu-id="550e3-138">**b**</span></span> <br/> |<span data-ttu-id="550e3-139">int curto não assinado</span><span class="sxs-lookup"><span data-stu-id="550e3-139">unsigned short int</span></span>  <br/> |
|<span data-ttu-id="550e3-140">PT_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="550e3-140">PT_CURRENCY</span></span>  <br/> |<span data-ttu-id="550e3-141">**atual**</span><span class="sxs-lookup"><span data-stu-id="550e3-141">**cur**</span></span> <br/> |[<span data-ttu-id="550e3-142">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="550e3-142">CURRENCY</span></span>](currency.md) <br/> |
|<span data-ttu-id="550e3-143">PT_APPTIME</span><span class="sxs-lookup"><span data-stu-id="550e3-143">PT_APPTIME</span></span>  <br/> |<span data-ttu-id="550e3-144">**em**</span><span class="sxs-lookup"><span data-stu-id="550e3-144">**at**</span></span> <br/> |<span data-ttu-id="550e3-145">double</span><span class="sxs-lookup"><span data-stu-id="550e3-145">double</span></span>  <br/> |
|<span data-ttu-id="550e3-146">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="550e3-146">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="550e3-147">**FT**</span><span class="sxs-lookup"><span data-stu-id="550e3-147">**ft**</span></span> <br/> |[<span data-ttu-id="550e3-148">FILETIME</span><span class="sxs-lookup"><span data-stu-id="550e3-148">FILETIME</span></span>](filetime.md) <br/> |
|<span data-ttu-id="550e3-149">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="550e3-149">PT_STRING8</span></span>  <br/> |<span data-ttu-id="550e3-150">**lpszA**</span><span class="sxs-lookup"><span data-stu-id="550e3-150">**lpszA**</span></span> <br/> |<span data-ttu-id="550e3-151">LPSTR</span><span class="sxs-lookup"><span data-stu-id="550e3-151">LPSTR</span></span>  <br/> |
|<span data-ttu-id="550e3-152">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="550e3-152">PT_BINARY</span></span>  <br/> |<span data-ttu-id="550e3-153">**bin**</span><span class="sxs-lookup"><span data-stu-id="550e3-153">**bin**</span></span> <br/> |<span data-ttu-id="550e3-154">BYTE [matriz]</span><span class="sxs-lookup"><span data-stu-id="550e3-154">BYTE [array]</span></span>  <br/> |
|<span data-ttu-id="550e3-155">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="550e3-155">PT_UNICODE</span></span>  <br/> |<span data-ttu-id="550e3-156">**lpszW**</span><span class="sxs-lookup"><span data-stu-id="550e3-156">**lpszW**</span></span> <br/> |<span data-ttu-id="550e3-157">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="550e3-157">LPWSTR</span></span>  <br/> |
|<span data-ttu-id="550e3-158">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="550e3-158">PT_CLSID</span></span>  <br/> |<span data-ttu-id="550e3-159">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="550e3-159">**lpguid**</span></span> <br/> |<span data-ttu-id="550e3-160">LPGUID</span><span class="sxs-lookup"><span data-stu-id="550e3-160">LPGUID</span></span>  <br/> |
|<span data-ttu-id="550e3-161">PT_I8 ou PT_LONGLONG</span><span class="sxs-lookup"><span data-stu-id="550e3-161">PT_I8 or PT_LONGLONG</span></span>  <br/> |<span data-ttu-id="550e3-162">**li**</span><span class="sxs-lookup"><span data-stu-id="550e3-162">**li**</span></span> <br/> |<span data-ttu-id="550e3-163">**LARGE_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="550e3-163">**LARGE_INTEGER**</span></span> <br/> |
|<span data-ttu-id="550e3-164">PT_MV_I2</span><span class="sxs-lookup"><span data-stu-id="550e3-164">PT_MV_I2</span></span>  <br/> |<span data-ttu-id="550e3-165">**MVi**</span><span class="sxs-lookup"><span data-stu-id="550e3-165">**MVi**</span></span> <br/> |[<span data-ttu-id="550e3-166">SShortArray</span><span class="sxs-lookup"><span data-stu-id="550e3-166">SShortArray</span></span>](sshortarray.md) <br/> |
|<span data-ttu-id="550e3-167">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="550e3-167">PT_MV_LONG</span></span>  <br/> |<span data-ttu-id="550e3-168">**MVI**</span><span class="sxs-lookup"><span data-stu-id="550e3-168">**MVI**</span></span> <br/> |[<span data-ttu-id="550e3-169">SLongArray</span><span class="sxs-lookup"><span data-stu-id="550e3-169">SLongArray</span></span>](slongarray.md) <br/> |
|<span data-ttu-id="550e3-170">PT_MV_R4</span><span class="sxs-lookup"><span data-stu-id="550e3-170">PT_MV_R4</span></span>  <br/> |<span data-ttu-id="550e3-171">**MVflt**</span><span class="sxs-lookup"><span data-stu-id="550e3-171">**MVflt**</span></span> <br/> |[<span data-ttu-id="550e3-172">SRealArray</span><span class="sxs-lookup"><span data-stu-id="550e3-172">SRealArray</span></span>](srealarray.md) <br/> |
|<span data-ttu-id="550e3-173">PT_MV_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="550e3-173">PT_MV_DOUBLE</span></span>  <br/> |<span data-ttu-id="550e3-174">**MVdbl**</span><span class="sxs-lookup"><span data-stu-id="550e3-174">**MVdbl**</span></span> <br/> |[<span data-ttu-id="550e3-175">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="550e3-175">SDoubleArray</span></span>](sdoublearray.md) <br/> |
|<span data-ttu-id="550e3-176">PT_MV_CURRENCY</span><span class="sxs-lookup"><span data-stu-id="550e3-176">PT_MV_CURRENCY</span></span>  <br/> |<span data-ttu-id="550e3-177">**MVcur**</span><span class="sxs-lookup"><span data-stu-id="550e3-177">**MVcur**</span></span> <br/> |[<span data-ttu-id="550e3-178">SCurrencyArray</span><span class="sxs-lookup"><span data-stu-id="550e3-178">SCurrencyArray</span></span>](scurrencyarray.md) <br/> |
|<span data-ttu-id="550e3-179">PT_MV_APPTIME</span><span class="sxs-lookup"><span data-stu-id="550e3-179">PT_MV_APPTIME</span></span>  <br/> |<span data-ttu-id="550e3-180">**MVat**</span><span class="sxs-lookup"><span data-stu-id="550e3-180">**MVat**</span></span> <br/> |[<span data-ttu-id="550e3-181">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="550e3-181">SAppTimeArray</span></span>](sapptimearray.md) <br/> |
|<span data-ttu-id="550e3-182">PT_MV_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="550e3-182">PT_MV_SYSTIME</span></span>  <br/> |<span data-ttu-id="550e3-183">**MVft**</span><span class="sxs-lookup"><span data-stu-id="550e3-183">**MVft**</span></span> <br/> |[<span data-ttu-id="550e3-184">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="550e3-184">SDateTimeArray</span></span>](sdatetimearray.md) <br/> |
|<span data-ttu-id="550e3-185">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="550e3-185">PT_MV_BINARY</span></span>  <br/> |<span data-ttu-id="550e3-186">**MVbin**</span><span class="sxs-lookup"><span data-stu-id="550e3-186">**MVbin**</span></span> <br/> |[<span data-ttu-id="550e3-187">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="550e3-187">SBinaryArray</span></span>](sbinaryarray.md) <br/> |
|<span data-ttu-id="550e3-188">PT_MV_STRING8</span><span class="sxs-lookup"><span data-stu-id="550e3-188">PT_MV_STRING8</span></span>  <br/> |<span data-ttu-id="550e3-189">**MVszA**</span><span class="sxs-lookup"><span data-stu-id="550e3-189">**MVszA**</span></span> <br/> |[<span data-ttu-id="550e3-190">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="550e3-190">SLPSTRArray</span></span>](slpstrarray.md) <br/> |
|<span data-ttu-id="550e3-191">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="550e3-191">PT_MV_UNICODE</span></span>  <br/> |<span data-ttu-id="550e3-192">**MVszW**</span><span class="sxs-lookup"><span data-stu-id="550e3-192">**MVszW**</span></span> <br/> |[<span data-ttu-id="550e3-193">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="550e3-193">SWStringArray</span></span>](swstringarray.md) <br/> |
|<span data-ttu-id="550e3-194">PT_MV_CLSID</span><span class="sxs-lookup"><span data-stu-id="550e3-194">PT_MV_CLSID</span></span>  <br/> |<span data-ttu-id="550e3-195">**MVguid**</span><span class="sxs-lookup"><span data-stu-id="550e3-195">**MVguid**</span></span> <br/> |[<span data-ttu-id="550e3-196">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="550e3-196">SGuidArray</span></span>](sguidarray.md) <br/> |
|<span data-ttu-id="550e3-197">PT_MV_I8</span><span class="sxs-lookup"><span data-stu-id="550e3-197">PT_MV_I8</span></span>  <br/> |<span data-ttu-id="550e3-198">**MVli**</span><span class="sxs-lookup"><span data-stu-id="550e3-198">**MVli**</span></span> <br/> |[<span data-ttu-id="550e3-199">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="550e3-199">SLargeIntegerArray</span></span>](slargeintegerarray.md) <br/> |
|<span data-ttu-id="550e3-200">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="550e3-200">PT_ERROR</span></span>  <br/> |<span data-ttu-id="550e3-201">**err**</span><span class="sxs-lookup"><span data-stu-id="550e3-201">**err**</span></span> <br/> |[<span data-ttu-id="550e3-202">SCODE</span><span class="sxs-lookup"><span data-stu-id="550e3-202">SCODE</span></span>](scode.md) <br/> |
|<span data-ttu-id="550e3-203">PT_NULL ou PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="550e3-203">PT_NULL or PT_OBJECT</span></span>  <br/> |<span data-ttu-id="550e3-204">**x**</span><span class="sxs-lookup"><span data-stu-id="550e3-204">**x**</span></span> <br/> |<span data-ttu-id="550e3-205">Longas</span><span class="sxs-lookup"><span data-stu-id="550e3-205">LONG</span></span>  <br/> |
|<span data-ttu-id="550e3-206">PT_PTR</span><span class="sxs-lookup"><span data-stu-id="550e3-206">PT_PTR</span></span>  <br/> |<span data-ttu-id="550e3-207">**lpv**</span><span class="sxs-lookup"><span data-stu-id="550e3-207">**lpv**</span></span> <br/> |<span data-ttu-id="550e3-208">VOID\*</span><span class="sxs-lookup"><span data-stu-id="550e3-208">VOID \*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="550e3-209">Comentários</span><span class="sxs-lookup"><span data-stu-id="550e3-209">Remarks</span></span>

<span data-ttu-id="550e3-210">O membro **ulPropTag** é composto por duas partes:</span><span class="sxs-lookup"><span data-stu-id="550e3-210">The **ulPropTag** member is made up of two parts:</span></span> 
  
- <span data-ttu-id="550e3-211">Um identificador nos superiores 16 bits.</span><span class="sxs-lookup"><span data-stu-id="550e3-211">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="550e3-212">Um tipo nos ordem baixa 16 bits.</span><span class="sxs-lookup"><span data-stu-id="550e3-212">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="550e3-213">O identificador é um valor numérico dentro de um determinado intervalo.</span><span class="sxs-lookup"><span data-stu-id="550e3-213">The identifier is a numeric value within a particular range.</span></span> <span data-ttu-id="550e3-214">MAPI define os intervalos para os identificadores descrever o que a propriedade é usada para e quem é responsável por manter a ele.</span><span class="sxs-lookup"><span data-stu-id="550e3-214">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="550e3-215">MAPI define restrições para cada um das marcas de propriedade ao qual ele oferece suporte no arquivo de cabeçalho Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="550e3-215">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="550e3-216">O tipo indica o formato para o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="550e3-216">The type indicates the format for the property's value.</span></span> <span data-ttu-id="550e3-217">MAPI define as constantes para cada um dos tipos de propriedade que ele suporta no arquivo de cabeçalho Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="550e3-217">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="550e3-218">Para obter uma lista completa dos intervalos de propriedade válidos para tipos de propriedade e identificadores, consulte o Apêndice [tipos e identificadores de propriedade](property-identifiers-and-types.md) .</span><span class="sxs-lookup"><span data-stu-id="550e3-218">For a complete list of the valid property ranges for identifiers and property types, see the [Property Identifiers and Types](property-identifiers-and-types.md) appendix.</span></span> 
  
<span data-ttu-id="550e3-219">O membro **dwAlignPad** é usado como preenchimento para tornar o alinhamento adequado claro que em computadores que exijam o alinhamento de 8 bytes para valores de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="550e3-219">The **dwAlignPad** member is used as padding to make sure proper alignment on computers that require 8-byte alignment for 8-byte values.</span></span> <span data-ttu-id="550e3-220">Os desenvolvedores que escrever código nesses computadores devem usar rotinas de alocação de memória que alocar as matrizes **SPropValue** nos limites de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="550e3-220">Developers who write code on such computers should use memory allocation routines that allocate the **SPropValue** arrays on 8-byte boundaries.</span></span> 
  
<span data-ttu-id="550e3-221">Para obter mais informações, consulte [Visão geral do tipo de propriedade de MAPI](mapi-property-type-overview.md) e [Atualizar propriedades de MAPI](updating-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="550e3-221">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Updating MAPI Properties](updating-mapi-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="550e3-222">Confira também</span><span class="sxs-lookup"><span data-stu-id="550e3-222">See also</span></span>



[<span data-ttu-id="550e3-223">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="550e3-223">MAPI Structures</span></span>](mapi-structures.md)

