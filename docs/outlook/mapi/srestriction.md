---
title: SRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRestriction
api_type:
- COM
ms.assetid: c12b4409-da6f-480b-87af-1e5baea2e8bd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5f8a76cb317ac9bf1b6a4dc4a92b6d6f0098e1d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577398"
---
# <a name="srestriction"></a><span data-ttu-id="c313e-103">SRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-103">SRestriction</span></span>

  
  
<span data-ttu-id="c313e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c313e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c313e-105">Descreve um filtro para limitar o modo de exibição de uma tabela às linhas específicas.</span><span class="sxs-lookup"><span data-stu-id="c313e-105">Describes a filter for limiting the view of a table to particular rows.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c313e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c313e-106">Header file:</span></span>  <br/> |<span data-ttu-id="c313e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c313e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRestriction
{
  ULONG rt;
  union
  {
    SComparePropsRestriction resCompareProps;
    SAndRestriction resAnd;
    SOrRestriction resOr;
    SNotRestriction resNot;
    SContentRestriction resContent;
    SPropertyRestriction resProperty;
    SBitMaskRestriction resBitMask;
    SSizeRestriction resSize;
    SExistRestriction resExist;
    SSubRestriction resSub;
    SCommentRestriction resComment;
  } res;
} SRestriction;

```

## <a name="members"></a><span data-ttu-id="c313e-108">Members</span><span class="sxs-lookup"><span data-stu-id="c313e-108">Members</span></span>

 <span data-ttu-id="c313e-109">**RT**</span><span class="sxs-lookup"><span data-stu-id="c313e-109">**rt**</span></span>
  
> <span data-ttu-id="c313e-110">O tipo de restrição.</span><span class="sxs-lookup"><span data-stu-id="c313e-110">The restriction type.</span></span> <span data-ttu-id="c313e-111">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="c313e-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="c313e-112">RES_AND</span><span class="sxs-lookup"><span data-stu-id="c313e-112">RES_AND</span></span> 
  
> <span data-ttu-id="c313e-113">Uma restrição **AND** , que se aplica a uma operação de **AND** bit a bit a uma restrição.</span><span class="sxs-lookup"><span data-stu-id="c313e-113">An **AND** restriction, which applies a bitwise **AND** operation to a restriction.</span></span> 
    
<span data-ttu-id="c313e-114">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="c313e-114">RES_BITMASK</span></span> 
  
> <span data-ttu-id="c313e-115">Uma restrição de bitmask que se aplica a uma máscara de bits para um valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c313e-115">A bitmask restriction, which applies a bitmask to a property value.</span></span>
    
<span data-ttu-id="c313e-116">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="c313e-116">RES_COMMENT</span></span> 
  
> <span data-ttu-id="c313e-117">Uma restrição de comentário, que associa um comentário uma restrição.</span><span class="sxs-lookup"><span data-stu-id="c313e-117">A comment restriction, which associates a comment with a restriction.</span></span>
    
<span data-ttu-id="c313e-118">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="c313e-118">RES_COMPAREPROPS</span></span> 
  
> <span data-ttu-id="c313e-119">Uma restrição de comparação de propriedade, que compara dois valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c313e-119">A property comparison restriction, which compares two property values.</span></span>
    
<span data-ttu-id="c313e-120">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="c313e-120">RES_CONTENT</span></span> 
  
> <span data-ttu-id="c313e-121">Uma restrição de conteúdo, que procura um valor de propriedade para conteúdo específico.</span><span class="sxs-lookup"><span data-stu-id="c313e-121">A content restriction, which searches a property value for specific content.</span></span>
    
<span data-ttu-id="c313e-122">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="c313e-122">RES_EXIST</span></span> 
  
> <span data-ttu-id="c313e-123">Uma restrição da lista, que determina se uma propriedade é suportada.</span><span class="sxs-lookup"><span data-stu-id="c313e-123">An exist restriction, which determines whether a property is supported.</span></span>
    
<span data-ttu-id="c313e-124">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="c313e-124">RES_NOT</span></span> 
  
> <span data-ttu-id="c313e-125">Uma **não** restrição, que se aplica a uma operação **não é** lógica para uma restrição.</span><span class="sxs-lookup"><span data-stu-id="c313e-125">A **NOT** restriction, which applies a logical **NOT** operation to a restriction.</span></span> 
    
<span data-ttu-id="c313e-126">RES_OR</span><span class="sxs-lookup"><span data-stu-id="c313e-126">RES_OR</span></span> 
  
> <span data-ttu-id="c313e-127">Uma restrição **ou** , que se aplica a uma operação **OR** lógica para uma restrição.</span><span class="sxs-lookup"><span data-stu-id="c313e-127">An **OR** restriction, which applies a logical **OR** operation to a restriction.</span></span> 
    
<span data-ttu-id="c313e-128">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="c313e-128">RES_PROPERTY</span></span> 
  
> <span data-ttu-id="c313e-129">Uma restrição de propriedade, que determina se um valor da propriedade corresponde a um determinado valor.</span><span class="sxs-lookup"><span data-stu-id="c313e-129">A property restriction, which determines whether a property value matches a particular value.</span></span>
    
<span data-ttu-id="c313e-130">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="c313e-130">RES_SIZE</span></span> 
  
> <span data-ttu-id="c313e-131">Uma restrição de tamanho, que determina se um valor de propriedade é de um determinado tamanho.</span><span class="sxs-lookup"><span data-stu-id="c313e-131">A size restriction, which determines whether a property value is a particular size.</span></span>
    
<span data-ttu-id="c313e-132">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="c313e-132">RES_SUBRESTRICTION</span></span> 
  
> <span data-ttu-id="c313e-133">Uma restrição de objeto sub, que se aplica a uma restrição de anexos ou os destinatários de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="c313e-133">A sub-object restriction, which applies a restriction to a message's attachments or recipients.</span></span>
    
 <span data-ttu-id="c313e-134">**res**</span><span class="sxs-lookup"><span data-stu-id="c313e-134">**res**</span></span>
  
> <span data-ttu-id="c313e-135">União de estruturas de restrição descrevendo o filtro a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="c313e-135">Union of restriction structures describing the filter to be applied.</span></span> <span data-ttu-id="c313e-136">A estrutura específica incluída no membro **rec** depende do valor do membro **rt** .</span><span class="sxs-lookup"><span data-stu-id="c313e-136">The specific structure included in the **res** member depends on the value of the **rt** member.</span></span> <span data-ttu-id="c313e-137">O mapeamento entre o tipo de restrição e a estrutura está listado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c313e-137">The mapping between restriction type and structure is listed in the following table.</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="c313e-138">**Tipo de restrição**</span><span class="sxs-lookup"><span data-stu-id="c313e-138">**Restriction type**</span></span> <br/> |<span data-ttu-id="c313e-139">**Estrutura de restrição**</span><span class="sxs-lookup"><span data-stu-id="c313e-139">**Restriction structure**</span></span> <br/> |
|<span data-ttu-id="c313e-140">RES_AND</span><span class="sxs-lookup"><span data-stu-id="c313e-140">RES_AND</span></span>  <br/> |[<span data-ttu-id="c313e-141">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-141">SAndRestriction</span></span>](sandrestriction.md) <br/> |
|<span data-ttu-id="c313e-142">RES_BITMASK</span><span class="sxs-lookup"><span data-stu-id="c313e-142">RES_BITMASK</span></span>  <br/> |[<span data-ttu-id="c313e-143">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-143">SBitMaskRestriction</span></span>](sbitmaskrestriction.md) <br/> |
|<span data-ttu-id="c313e-144">RES_COMMENT</span><span class="sxs-lookup"><span data-stu-id="c313e-144">RES_COMMENT</span></span>  <br/> |[<span data-ttu-id="c313e-145">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-145">SCommentRestriction</span></span>](scommentrestriction.md) <br/> |
|<span data-ttu-id="c313e-146">RES_COMPAREPROPS</span><span class="sxs-lookup"><span data-stu-id="c313e-146">RES_COMPAREPROPS</span></span>  <br/> |[<span data-ttu-id="c313e-147">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-147">SComparePropsRestriction</span></span>](scomparepropsrestriction.md) <br/> |
|<span data-ttu-id="c313e-148">RES_CONTENT</span><span class="sxs-lookup"><span data-stu-id="c313e-148">RES_CONTENT</span></span>  <br/> |[<span data-ttu-id="c313e-149">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-149">SContentRestriction</span></span>](scontentrestriction.md) <br/> |
|<span data-ttu-id="c313e-150">RES_EXIST</span><span class="sxs-lookup"><span data-stu-id="c313e-150">RES_EXIST</span></span>  <br/> |[<span data-ttu-id="c313e-151">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-151">SExistRestriction</span></span>](sexistrestriction.md) <br/> |
|<span data-ttu-id="c313e-152">RES_NOT</span><span class="sxs-lookup"><span data-stu-id="c313e-152">RES_NOT</span></span>  <br/> |[<span data-ttu-id="c313e-153">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-153">SNotRestriction</span></span>](snotrestriction.md) <br/> |
|<span data-ttu-id="c313e-154">RES_OR</span><span class="sxs-lookup"><span data-stu-id="c313e-154">RES_OR</span></span>  <br/> |[<span data-ttu-id="c313e-155">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-155">SOrRestriction</span></span>](sorrestriction.md) <br/> |
|<span data-ttu-id="c313e-156">RES_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="c313e-156">RES_PROPERTY</span></span>  <br/> |[<span data-ttu-id="c313e-157">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-157">SPropertyRestriction</span></span>](spropertyrestriction.md) <br/> |
|<span data-ttu-id="c313e-158">RES_SIZE</span><span class="sxs-lookup"><span data-stu-id="c313e-158">RES_SIZE</span></span>  <br/> |[<span data-ttu-id="c313e-159">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-159">SSizeRestriction</span></span>](ssizerestriction.md) <br/> |
|<span data-ttu-id="c313e-160">RES_SUBRESTRICTION</span><span class="sxs-lookup"><span data-stu-id="c313e-160">RES_SUBRESTRICTION</span></span>  <br/> |[<span data-ttu-id="c313e-161">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-161">SSubRestriction</span></span>](ssubrestriction.md) <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c313e-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="c313e-162">Remarks</span></span>

<span data-ttu-id="c313e-163">Os clientes usar uma estrutura **SRestriction** para limitar o número e tipo de linhas no seu modo de exibição de uma tabela e procurar mensagens específicas em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="c313e-163">Clients use an **SRestriction** structure to limit the number and type of rows in their view of a table and to search for specific messages in a folder.</span></span> <span data-ttu-id="c313e-164">Para impor a limitação em uma tabela, os clientes chamam [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="c313e-164">To impose the limitation on a table, clients call either [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> <span data-ttu-id="c313e-165">Para impor a limitação em uma pasta, clientes chamar o método de [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) da pasta.</span><span class="sxs-lookup"><span data-stu-id="c313e-165">To impose the limitation on a folder, clients call the folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method.</span></span> 
  
<span data-ttu-id="c313e-166">Para obter informações sobre como usar as restrições com tabelas, consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="c313e-166">For information about how to use restrictions with tables, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c313e-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="c313e-167">See also</span></span>



[<span data-ttu-id="c313e-168">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-168">SAndRestriction</span></span>](sandrestriction.md)
  
[<span data-ttu-id="c313e-169">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-169">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
  
[<span data-ttu-id="c313e-170">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-170">SCommentRestriction</span></span>](scommentrestriction.md)
  
[<span data-ttu-id="c313e-171">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-171">SComparePropsRestriction</span></span>](scomparepropsrestriction.md)
  
[<span data-ttu-id="c313e-172">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-172">SContentRestriction</span></span>](scontentrestriction.md)
  
[<span data-ttu-id="c313e-173">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-173">SExistRestriction</span></span>](sexistrestriction.md)
  
[<span data-ttu-id="c313e-174">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-174">SNotRestriction</span></span>](snotrestriction.md)
  
[<span data-ttu-id="c313e-175">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-175">SOrRestriction</span></span>](sorrestriction.md)
  
[<span data-ttu-id="c313e-176">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-176">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="c313e-177">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-177">SSizeRestriction</span></span>](ssizerestriction.md)
  
[<span data-ttu-id="c313e-178">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="c313e-178">SSubRestriction</span></span>](ssubrestriction.md)


[<span data-ttu-id="c313e-179">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="c313e-179">MAPI Structures</span></span>](mapi-structures.md)

