---
title: Propriedade canônica PidTagMemberRights
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberRights
api_type:
- HeaderDef
ms.assetid: 3e526b93-1f64-41ea-b43c-5b03fe1c56ed
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dcbf8a323f5178a5a2e39d0963dd19415ab835bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342691"
---
# <a name="pidtagmemberrights-canonical-property"></a><span data-ttu-id="2c260-103">Propriedade canônica PidTagMemberRights</span><span class="sxs-lookup"><span data-stu-id="2c260-103">PidTagMemberRights Canonical Property</span></span>

  
  
<span data-ttu-id="2c260-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c260-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c260-105">Contém um conjunto de bits que indica os direitos desse membro em uma pasta ou caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="2c260-105">Contains a set of bits that indicated the rights of this member on a folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c260-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2c260-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c260-107">PR_MEMBER_RIGHTS</span><span class="sxs-lookup"><span data-stu-id="2c260-107">PR_MEMBER_RIGHTS</span></span>  <br/> |
|<span data-ttu-id="2c260-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2c260-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2c260-109">0x6673</span><span class="sxs-lookup"><span data-stu-id="2c260-109">0x6673</span></span>  <br/> |
|<span data-ttu-id="2c260-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2c260-110">Data type:</span></span>  <br/> |<span data-ttu-id="2c260-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2c260-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2c260-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2c260-112">Area:</span></span>  <br/> |<span data-ttu-id="2c260-113">Controle de Acesso</span><span class="sxs-lookup"><span data-stu-id="2c260-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c260-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c260-114">Remarks</span></span>

<span data-ttu-id="2c260-115">Essa propriedade é usada pela interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) para definir direitos de um membro em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="2c260-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to define rights of a member on a folder.</span></span> <span data-ttu-id="2c260-116">Esses direitos podem ser exibidos e modificados.</span><span class="sxs-lookup"><span data-stu-id="2c260-116">These rights can be displayed and modified.</span></span> <span data-ttu-id="2c260-117">Os seguintes valores são direitos definidos para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="2c260-117">The following values are rights defined for this property.</span></span> 
  
<span data-ttu-id="2c260-118">readAny</span><span class="sxs-lookup"><span data-stu-id="2c260-118">frightsReadAny</span></span>
  
> <span data-ttu-id="2c260-119">O membro pode ler todas as mensagens.</span><span class="sxs-lookup"><span data-stu-id="2c260-119">Member can read any messages.</span></span>
    
<span data-ttu-id="2c260-120">dasCreate</span><span class="sxs-lookup"><span data-stu-id="2c260-120">frightsCreate</span></span>
  
> <span data-ttu-id="2c260-121">O membro pode criar mensagens.</span><span class="sxs-lookup"><span data-stu-id="2c260-121">Member can create messages.</span></span>
    
<span data-ttu-id="2c260-122">dasEditOwned</span><span class="sxs-lookup"><span data-stu-id="2c260-122">frightsEditOwned</span></span>
  
> <span data-ttu-id="2c260-123">O membro pode editar todas as mensagens pertencentes ao usuário.</span><span class="sxs-lookup"><span data-stu-id="2c260-123">Member can edit any messages owned by the user.</span></span>
    
<span data-ttu-id="2c260-124">adletadosDeleteOwned</span><span class="sxs-lookup"><span data-stu-id="2c260-124">frightsDeleteOwned</span></span>
  
> <span data-ttu-id="2c260-125">O membro pode excluir todas as mensagens pertencentes ao usuário.</span><span class="sxs-lookup"><span data-stu-id="2c260-125">Member can delete any messages owned by the user.</span></span>
    
<span data-ttu-id="2c260-126">daSeditAny</span><span class="sxs-lookup"><span data-stu-id="2c260-126">frightsEditAny</span></span>
  
> <span data-ttu-id="2c260-127">O membro pode editar qualquer mensagem.</span><span class="sxs-lookup"><span data-stu-id="2c260-127">Member can edit any message.</span></span>
    
<span data-ttu-id="2c260-128">adlettasDeleteAny</span><span class="sxs-lookup"><span data-stu-id="2c260-128">frightsDeleteAny</span></span>
  
> <span data-ttu-id="2c260-129">O membro pode excluir qualquer mensagem.</span><span class="sxs-lookup"><span data-stu-id="2c260-129">Member can delete any message.</span></span>
    
<span data-ttu-id="2c260-130">wesCreateSubfolder</span><span class="sxs-lookup"><span data-stu-id="2c260-130">frightsCreateSubfolder</span></span>
  
> <span data-ttu-id="2c260-131">O membro pode criar subpastas para a pasta.</span><span class="sxs-lookup"><span data-stu-id="2c260-131">Member can create subfolders for the folder.</span></span>
    
<span data-ttu-id="2c260-132">ownsOwner</span><span class="sxs-lookup"><span data-stu-id="2c260-132">frightsOwner</span></span>
  
> <span data-ttu-id="2c260-133">O membro tem todos os direitos anteriores na pasta.</span><span class="sxs-lookup"><span data-stu-id="2c260-133">Member has all the previous rights on the folder.</span></span>
    
<span data-ttu-id="2c260-134">adsContact</span><span class="sxs-lookup"><span data-stu-id="2c260-134">frightsContact</span></span>
  
> <span data-ttu-id="2c260-135">O membro pode fazer com que seu nome apareça como contato na pasta.</span><span class="sxs-lookup"><span data-stu-id="2c260-135">Member can have your name appear as the contact on the folder.</span></span>
    
<span data-ttu-id="2c260-136">daVisible</span><span class="sxs-lookup"><span data-stu-id="2c260-136">frightsVisible</span></span>
  
> <span data-ttu-id="2c260-137">O membro pode ver que a pasta existe.</span><span class="sxs-lookup"><span data-stu-id="2c260-137">Member can see that the folder exists.</span></span>
    
<span data-ttu-id="2c260-138">rightsNone</span><span class="sxs-lookup"><span data-stu-id="2c260-138">rightsNone</span></span>
  
> <span data-ttu-id="2c260-139">O membro não tem direitos na pasta.</span><span class="sxs-lookup"><span data-stu-id="2c260-139">Member does not have rights on the folder.</span></span>
    
<span data-ttu-id="2c260-140">rightsReadOnly</span><span class="sxs-lookup"><span data-stu-id="2c260-140">rightsReadOnly</span></span>
  
> <span data-ttu-id="2c260-141">O membro pode ler qualquer mensagem na pasta.</span><span class="sxs-lookup"><span data-stu-id="2c260-141">Member can read any message in the folder.</span></span>
    
<span data-ttu-id="2c260-142">rightsReadWrite</span><span class="sxs-lookup"><span data-stu-id="2c260-142">rightsReadWrite</span></span>
  
> <span data-ttu-id="2c260-143">O membro pode ler e gravar em qualquer mensagem na pasta.</span><span class="sxs-lookup"><span data-stu-id="2c260-143">Member can read from and write to any message in the folder.</span></span>
    
<span data-ttu-id="2c260-144">rightsAll</span><span class="sxs-lookup"><span data-stu-id="2c260-144">rightsAll</span></span>
  
> <span data-ttu-id="2c260-145">O membro tem todos os direitos anteriores na pasta.</span><span class="sxs-lookup"><span data-stu-id="2c260-145">Member has all the previous rights on the folder.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="2c260-146">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c260-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c260-147">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="2c260-147">Protocol specifications</span></span>

<span data-ttu-id="2c260-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c260-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c260-149">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2c260-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2c260-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c260-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c260-151">Lida com operações de pasta.</span><span class="sxs-lookup"><span data-stu-id="2c260-151">Handles folder operations.</span></span>
    
<span data-ttu-id="2c260-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c260-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c260-153">Lida com a recuperação de listas de permissões de pasta armazenadas no servidor.</span><span class="sxs-lookup"><span data-stu-id="2c260-153">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="2c260-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c260-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c260-155">Especifica métodos para conectar e configurar caixas de correio como representantes e interações com itens de mensagem e calendário quando eles agem em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="2c260-155">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2c260-156">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="2c260-156">Header files</span></span>

<span data-ttu-id="2c260-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c260-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c260-158">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2c260-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="2c260-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2c260-159">Mapitags.h</span></span>
  
> <span data-ttu-id="2c260-160">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="2c260-160">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c260-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c260-161">See also</span></span>



[<span data-ttu-id="2c260-162">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2c260-162">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="2c260-163">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2c260-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c260-164">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2c260-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c260-165">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2c260-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c260-166">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2c260-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

