---
title: Propriedade canônica PidTagDisplayTypeEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTypeEx
api_type:
- HeaderDef
ms.assetid: 23074402-6ac1-47f1-8a49-b8909f98a26e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a21eecfb1bf3bc4f09fc5becb9a4a99a97193330
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769207"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a><span data-ttu-id="b403a-103">Propriedade canônica PidTagDisplayTypeEx</span><span class="sxs-lookup"><span data-stu-id="b403a-103">PidTagDisplayTypeEx Canonical Property</span></span>

  
  
<span data-ttu-id="b403a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b403a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b403a-105">Contém o tipo de uma entrada, com relação a entrada como deve ser exibida em uma linha em uma tabela para a lista de endereços Global.</span><span class="sxs-lookup"><span data-stu-id="b403a-105">Contains the type of an entry, with respect to how the entry should be displayed in a row in a table for the Global Address List.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b403a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b403a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b403a-107">PR_DISPLAY_TYPE_EX</span><span class="sxs-lookup"><span data-stu-id="b403a-107">PR_DISPLAY_TYPE_EX</span></span>  <br/> |
|<span data-ttu-id="b403a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b403a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b403a-109">0x3905</span><span class="sxs-lookup"><span data-stu-id="b403a-109">0x3905</span></span>  <br/> |
|<span data-ttu-id="b403a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b403a-110">Data type:</span></span>  <br/> |<span data-ttu-id="b403a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b403a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b403a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b403a-112">Area:</span></span>  <br/> |<span data-ttu-id="b403a-113">Catálogo de endereços MAPI</span><span class="sxs-lookup"><span data-stu-id="b403a-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b403a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b403a-114">Remarks</span></span>

<span data-ttu-id="b403a-115">Essa propriedade especifica o tipo de uma entrada, com relação a como ele deve ser exibido na lista de endereços Global.</span><span class="sxs-lookup"><span data-stu-id="b403a-115">This property specifies the type of an entry, with respect to how it should be displayed in the Global Address List.</span></span> <span data-ttu-id="b403a-116">Ele fornece informações adicionais que não podem ser representadas em **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b403a-116">It provides additional information that cannot be represented in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
  
> [!NOTE]
> <span data-ttu-id="b403a-117">Os valores de **PR_DISPLAY_TYPE** e essa propriedade começam com "DT_" e definidos no Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="b403a-117">The values of both **PR_DISPLAY_TYPE** and this property begin with "DT_" and are defined in Mapitags.h.</span></span> <span data-ttu-id="b403a-118">Todos os valores não documentados são reservados para MAPI.</span><span class="sxs-lookup"><span data-stu-id="b403a-118">All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="b403a-119">Aplicativos cliente não devem definir qualquer novos valores e devem estar preparados para lidar com um valor não documentado.</span><span class="sxs-lookup"><span data-stu-id="b403a-119">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
<span data-ttu-id="b403a-120">Há algumas macros que podem ajudar a determinar os atributos de um objeto como se ele está local, remoto ou segurança controlada.</span><span class="sxs-lookup"><span data-stu-id="b403a-120">There are some macros that can help determine attributes of an object such as whether it is local, remote, or security-controlled.</span></span> <span data-ttu-id="b403a-121">Estas macros incluem:</span><span class="sxs-lookup"><span data-stu-id="b403a-121">These macros include:</span></span> 
  
|<span data-ttu-id="b403a-122">**Macro**</span><span class="sxs-lookup"><span data-stu-id="b403a-122">**Macro**</span></span>|<span data-ttu-id="b403a-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b403a-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b403a-124">DTE_FLAG_REMOTE_VALID</span><span class="sxs-lookup"><span data-stu-id="b403a-124">DTE_FLAG_REMOTE_VALID</span></span>  <br/> |<span data-ttu-id="b403a-125">0x80000000)</span><span class="sxs-lookup"><span data-stu-id="b403a-125">0x80000000)</span></span>  <br/> |
|<span data-ttu-id="b403a-126">DTE_FLAG_ACL_CAPABLE</span><span class="sxs-lookup"><span data-stu-id="b403a-126">DTE_FLAG_ACL_CAPABLE</span></span>  <br/> |<span data-ttu-id="b403a-127">0x40000000</span><span class="sxs-lookup"><span data-stu-id="b403a-127">0x40000000</span></span>  <br/> |
|<span data-ttu-id="b403a-128">DTE_MASK_REMOTE</span><span class="sxs-lookup"><span data-stu-id="b403a-128">DTE_MASK_REMOTE</span></span>  <br/> |<span data-ttu-id="b403a-129">0x0000ff00</span><span class="sxs-lookup"><span data-stu-id="b403a-129">0x0000ff00</span></span>  <br/> |
|<span data-ttu-id="b403a-130">DTE_MASK_LOCAL</span><span class="sxs-lookup"><span data-stu-id="b403a-130">DTE_MASK_LOCAL</span></span>  <br/> |<span data-ttu-id="b403a-131">0x000000ff</span><span class="sxs-lookup"><span data-stu-id="b403a-131">0x000000ff</span></span>  <br/> |
|<span data-ttu-id="b403a-132">DTE_IS_REMOTE_VALID(v)</span><span class="sxs-lookup"><span data-stu-id="b403a-132">DTE_IS_REMOTE_VALID(v)</span></span>  <br/> |<span data-ttu-id="b403a-133">(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)</span><span class="sxs-lookup"><span data-stu-id="b403a-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span></span>  <br/> |
|<span data-ttu-id="b403a-134">DTE_IS_ACL_CAPABLE(v)</span><span class="sxs-lookup"><span data-stu-id="b403a-134">DTE_IS_ACL_CAPABLE(v)</span></span>  <br/> |<span data-ttu-id="b403a-135">(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))</span><span class="sxs-lookup"><span data-stu-id="b403a-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span></span>  <br/> |
|<span data-ttu-id="b403a-136">DTE_REMOTE(v)</span><span class="sxs-lookup"><span data-stu-id="b403a-136">DTE_REMOTE(v)</span></span>  <br/> |<span data-ttu-id="b403a-137">(((v) &amp; DTE_MASK_REMOTE) \> \> 8)</span><span class="sxs-lookup"><span data-stu-id="b403a-137">(((v) &amp; DTE_MASK_REMOTE) \>\> 8)</span></span>  <br/> |
|<span data-ttu-id="b403a-138">DTE_LOCAL(v)</span><span class="sxs-lookup"><span data-stu-id="b403a-138">DTE_LOCAL(v)</span></span>  <br/> |<span data-ttu-id="b403a-139">((v) &amp; DTE_MASK_LOCAL)</span><span class="sxs-lookup"><span data-stu-id="b403a-139">((v) &amp; DTE_MASK_LOCAL)</span></span>  <br/> |
|<span data-ttu-id="b403a-140">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="b403a-140">DT_ROOM</span></span>  <br/> |<span data-ttu-id="b403a-141">((ULONG) 0X00000007)</span><span class="sxs-lookup"><span data-stu-id="b403a-141">((ULONG) 0x00000007)</span></span>  <br/> |
|<span data-ttu-id="b403a-142">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="b403a-142">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="b403a-143">((ULONG) 0X00000008)</span><span class="sxs-lookup"><span data-stu-id="b403a-143">((ULONG) 0x00000008)</span></span>  <br/> |
|<span data-ttu-id="b403a-144">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b403a-144">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="b403a-145">((ULONG) 0X00000009)</span><span class="sxs-lookup"><span data-stu-id="b403a-145">((ULONG) 0x00000009)</span></span>  <br/> |
   
<span data-ttu-id="b403a-146">A seguir estão algumas observações sobre como usar essas macros.</span><span class="sxs-lookup"><span data-stu-id="b403a-146">The following are a few notes about how to use these macros.</span></span> 
  
- <span data-ttu-id="b403a-147">Para verificar se uma entrada é uma entrada remota em outra floresta, se aplicam a macro DTE_IS_REMOTE_VALID com o valor dessa propriedade para verificar se o sinalizador DTE_FLAG_REMOTE_VALID está definido na entrada.</span><span class="sxs-lookup"><span data-stu-id="b403a-147">To check whether an entry is a remote entry in another forest, apply the DTE_IS_REMOTE_VALID macro to the value of this property to check whether the DTE_FLAG_REMOTE_VALID flag is set in the entry.</span></span> <span data-ttu-id="b403a-148">Se for uma entrada remota, você pode então descobrir o tipo da entrada remoto usando a macro DTE_REMOTE.</span><span class="sxs-lookup"><span data-stu-id="b403a-148">If it is a remote entry, you can then find out the type of the remote entry by using the DTE_REMOTE macro.</span></span> 
    
- <span data-ttu-id="b403a-149">Em configurações de floresta única e entre florestas, quando **PR_DISPLAY_TYPE** tem o valor de DT_DISTLIST e DTE_IS_REMOTE_VALID for false, a aplicação de macro DTE_LOCAL com o valor dessa propriedade pode permitem que você identifique ainda mais o tipo do objeto como DT_DISTLIST (uma lista de distribuição) ou DT_SEC_DISTLIST (uma lista de distribuição de segurança).</span><span class="sxs-lookup"><span data-stu-id="b403a-149">In both single-forest and cross-forest configurations, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST, and DTE_IS_REMOTE_VALID is false, applying the macro DTE_LOCAL to the value of this property can let you further identify the type of the object as either DT_DISTLIST (a distribution list) or DT_SEC_DISTLIST (a security distribution list).</span></span> 
    
- <span data-ttu-id="b403a-150">Se você aplicar a macro DTE_LOCAL como o valor de **PR_DISPLAY_TYPE_EX** e retorna o tipo DT_REMOTE_MAILUSER, a entrada é uma entrada remota.</span><span class="sxs-lookup"><span data-stu-id="b403a-150">If you apply the macro DTE_LOCAL to the value of **PR_DISPLAY_TYPE_EX** and it returns the type DT_REMOTE_MAILUSER, then the entry is a remote entry.</span></span> 
    
- <span data-ttu-id="b403a-151">Em uma única floresta ou em uma configuração entre florestas onde a replicação é controlada por uma lista de controle de acesso (ACL), você pode usar a macro DTE_IS_ACL_CAPABLE para determinar se uma entrada é uma entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="b403a-151">In a single forest or in a cross-forest configuration where replication is controlled by an Access Control List (ACL), you can use the DTE_IS_ACL_CAPABLE macro to determine whether an entry is a security principal.</span></span>
    
<span data-ttu-id="b403a-152">Em uma configuração entre florestas, **PR_DISPLAY_TYPE** tem o valor de DT_REMOTE_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="b403a-152">In a cross-forest configuration, **PR_DISPLAY_TYPE** has the value of DT_REMOTE_MAILUSER.</span></span> <span data-ttu-id="b403a-153">A aplicação de macro DTE_REMOTE com o valor dessa propriedade pode permitem que você obtenha o tipo da entrada remoto.</span><span class="sxs-lookup"><span data-stu-id="b403a-153">Applying the macro DTE_REMOTE to the value of this property can let you obtain the type of the remote entry.</span></span> <span data-ttu-id="b403a-154">Os tipos possíveis de entrada remota são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="b403a-154">The possible types of remote entry are the following:</span></span> 
  
|<span data-ttu-id="b403a-155">**Tipo de entrada remoto**</span><span class="sxs-lookup"><span data-stu-id="b403a-155">**Type of Remote Entry**</span></span>|<span data-ttu-id="b403a-156">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b403a-156">**Value**</span></span>|<span data-ttu-id="b403a-157">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b403a-157">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b403a-158">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="b403a-158">DT_AGENT</span></span>  <br/> |<span data-ttu-id="b403a-159">((ULONG) 0X00000003)</span><span class="sxs-lookup"><span data-stu-id="b403a-159">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="b403a-160">Lista de distribuição dinâmica.</span><span class="sxs-lookup"><span data-stu-id="b403a-160">Dynamic distribution list.</span></span>  <br/> |
|<span data-ttu-id="b403a-161">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b403a-161">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="b403a-162">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="b403a-162">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="b403a-163">Lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="b403a-163">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="b403a-164">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="b403a-164">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="b403a-165">((ULONG) 0X00000008)</span><span class="sxs-lookup"><span data-stu-id="b403a-165">((ULONG) 0x00000008)</span></span>  <br/> |<span data-ttu-id="b403a-166">Equipamento, por exemplo, uma impressora ou em um projetor.</span><span class="sxs-lookup"><span data-stu-id="b403a-166">Equipment, for example, a printer or a projector.</span></span>  <br/> |
|<span data-ttu-id="b403a-167">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="b403a-167">DT_MAILUSER</span></span>  <br/> |<span data-ttu-id="b403a-168">((ULONG) 0X00000000)</span><span class="sxs-lookup"><span data-stu-id="b403a-168">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="b403a-169">Usuário com uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="b403a-169">User with a mailbox.</span></span>  <br/> |
|<span data-ttu-id="b403a-170">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="b403a-170">DT_REMOTE_MAILUSER</span></span>  <br/> |<span data-ttu-id="b403a-171">((ULONG) 0X00000000)</span><span class="sxs-lookup"><span data-stu-id="b403a-171">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="b403a-172">Uma entrada da lista de endereços na lista de endereços Global.</span><span class="sxs-lookup"><span data-stu-id="b403a-172">An address list entry in the Global Address List.</span></span>  <br/> |
|<span data-ttu-id="b403a-173">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="b403a-173">DT_ROOM</span></span>  <br/> |<span data-ttu-id="b403a-174">((ULONG) 0X00000007)</span><span class="sxs-lookup"><span data-stu-id="b403a-174">((ULONG) 0x00000007)</span></span>  <br/> |<span data-ttu-id="b403a-175">Sala de conferência.</span><span class="sxs-lookup"><span data-stu-id="b403a-175">Conference room.</span></span>  <br/> |
|<span data-ttu-id="b403a-176">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b403a-176">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="b403a-177">((ULONG) 0X00000009)</span><span class="sxs-lookup"><span data-stu-id="b403a-177">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="b403a-178">Lista de distribuição de segurança.</span><span class="sxs-lookup"><span data-stu-id="b403a-178">Security distribution list.</span></span>  <br/> |
   
<span data-ttu-id="b403a-179">Em ambos os uma única floresta e em uma entre florestas configuração, quando **PR_DISPLAY_TYPE** tem o valor de DT_DISTLIST e DTE_IS_REMOTE_VALID for false, a aplicação de macro DTE_LOCAL com o valor dessa propriedade pode permitem que você obtenha o tipo da lista de distribuição .</span><span class="sxs-lookup"><span data-stu-id="b403a-179">In both a single forest and in a cross-forest configuration, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST and DTE_IS_REMOTE_VALID is false, applying the DTE_LOCAL macro to the value of this property can let you obtain the type of the distribution list.</span></span> <span data-ttu-id="b403a-180">Os possíveis tipos de lista de distribuição são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="b403a-180">The possible types of distribution list are the following:</span></span> 
  
|<span data-ttu-id="b403a-181">**Tipo de lista de distribuição**</span><span class="sxs-lookup"><span data-stu-id="b403a-181">**Type of Distribution List**</span></span>|<span data-ttu-id="b403a-182">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b403a-182">**Value**</span></span>|<span data-ttu-id="b403a-183">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b403a-183">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b403a-184">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b403a-184">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="b403a-185">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="b403a-185">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="b403a-186">Lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="b403a-186">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="b403a-187">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="b403a-187">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="b403a-188">((ULONG) 0X00000009)</span><span class="sxs-lookup"><span data-stu-id="b403a-188">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="b403a-189">Lista de distribuição de segurança.</span><span class="sxs-lookup"><span data-stu-id="b403a-189">Security distribution list.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b403a-190">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b403a-190">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b403a-191">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b403a-191">Protocol specifications</span></span>

<span data-ttu-id="b403a-192">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b403a-192">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b403a-193">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b403a-193">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b403a-194">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b403a-194">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b403a-195">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="b403a-195">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b403a-196">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b403a-196">Header files</span></span>

<span data-ttu-id="b403a-197">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b403a-197">Mapidefs.h</span></span>
  
> <span data-ttu-id="b403a-198">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b403a-198">Provides data type definitions.</span></span>
    
<span data-ttu-id="b403a-199">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b403a-199">Mapitags.h</span></span>
  
> <span data-ttu-id="b403a-200">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="b403a-200">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b403a-201">Confira também</span><span class="sxs-lookup"><span data-stu-id="b403a-201">See also</span></span>



[<span data-ttu-id="b403a-202">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b403a-202">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b403a-203">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="b403a-203">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b403a-204">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b403a-204">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b403a-205">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b403a-205">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
