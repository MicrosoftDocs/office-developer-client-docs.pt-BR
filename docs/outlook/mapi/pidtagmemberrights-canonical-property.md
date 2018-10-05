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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397335"
---
# <a name="pidtagmemberrights-canonical-property"></a><span data-ttu-id="b0777-103">Propriedade canônica PidTagMemberRights</span><span class="sxs-lookup"><span data-stu-id="b0777-103">PidTagMemberRights Canonical Property</span></span>

  
  
<span data-ttu-id="b0777-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0777-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0777-105">Contém um conjunto de bits que indicado os direitos deste membro em uma pasta ou caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="b0777-105">Contains a set of bits that indicated the rights of this member on a folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0777-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b0777-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0777-107">PR_MEMBER_RIGHTS</span><span class="sxs-lookup"><span data-stu-id="b0777-107">PR_MEMBER_RIGHTS</span></span>  <br/> |
|<span data-ttu-id="b0777-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b0777-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b0777-109">0x6673</span><span class="sxs-lookup"><span data-stu-id="b0777-109">0x6673</span></span>  <br/> |
|<span data-ttu-id="b0777-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b0777-110">Data type:</span></span>  <br/> |<span data-ttu-id="b0777-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b0777-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b0777-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b0777-112">Area:</span></span>  <br/> |<span data-ttu-id="b0777-113">Controle de acesso</span><span class="sxs-lookup"><span data-stu-id="b0777-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0777-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0777-114">Remarks</span></span>

<span data-ttu-id="b0777-115">Essa propriedade é usada pela interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) para definir os direitos de um membro em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="b0777-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to define rights of a member on a folder.</span></span> <span data-ttu-id="b0777-116">Esses direitos podem ser exibidos e modificados.</span><span class="sxs-lookup"><span data-stu-id="b0777-116">These rights can be displayed and modified.</span></span> <span data-ttu-id="b0777-117">Os seguintes valores são definidos para esta propriedade de direitos.</span><span class="sxs-lookup"><span data-stu-id="b0777-117">The following values are rights defined for this property.</span></span> 
  
<span data-ttu-id="b0777-118">frightsReadAny</span><span class="sxs-lookup"><span data-stu-id="b0777-118">frightsReadAny</span></span>
  
> <span data-ttu-id="b0777-119">Membro pode ler todas as mensagens.</span><span class="sxs-lookup"><span data-stu-id="b0777-119">Member can read any messages.</span></span>
    
<span data-ttu-id="b0777-120">frightsCreate</span><span class="sxs-lookup"><span data-stu-id="b0777-120">frightsCreate</span></span>
  
> <span data-ttu-id="b0777-121">Membro pode criar mensagens.</span><span class="sxs-lookup"><span data-stu-id="b0777-121">Member can create messages.</span></span>
    
<span data-ttu-id="b0777-122">frightsEditOwned</span><span class="sxs-lookup"><span data-stu-id="b0777-122">frightsEditOwned</span></span>
  
> <span data-ttu-id="b0777-123">Membro pode editar a todas as mensagens pertencentes ao usuário.</span><span class="sxs-lookup"><span data-stu-id="b0777-123">Member can edit any messages owned by the user.</span></span>
    
<span data-ttu-id="b0777-124">frightsDeleteOwned</span><span class="sxs-lookup"><span data-stu-id="b0777-124">frightsDeleteOwned</span></span>
  
> <span data-ttu-id="b0777-125">Membro pode excluir todas as mensagens pertencentes ao usuário.</span><span class="sxs-lookup"><span data-stu-id="b0777-125">Member can delete any messages owned by the user.</span></span>
    
<span data-ttu-id="b0777-126">frightsEditAny</span><span class="sxs-lookup"><span data-stu-id="b0777-126">frightsEditAny</span></span>
  
> <span data-ttu-id="b0777-127">Membro pode editar qualquer mensagem.</span><span class="sxs-lookup"><span data-stu-id="b0777-127">Member can edit any message.</span></span>
    
<span data-ttu-id="b0777-128">frightsDeleteAny</span><span class="sxs-lookup"><span data-stu-id="b0777-128">frightsDeleteAny</span></span>
  
> <span data-ttu-id="b0777-129">Membro pode excluir qualquer mensagem.</span><span class="sxs-lookup"><span data-stu-id="b0777-129">Member can delete any message.</span></span>
    
<span data-ttu-id="b0777-130">frightsCreateSubfolder</span><span class="sxs-lookup"><span data-stu-id="b0777-130">frightsCreateSubfolder</span></span>
  
> <span data-ttu-id="b0777-131">Membro pode criar subpastas da pasta.</span><span class="sxs-lookup"><span data-stu-id="b0777-131">Member can create subfolders for the folder.</span></span>
    
<span data-ttu-id="b0777-132">frightsOwner</span><span class="sxs-lookup"><span data-stu-id="b0777-132">frightsOwner</span></span>
  
> <span data-ttu-id="b0777-133">Membro tem todos os direitos anteriores na pasta.</span><span class="sxs-lookup"><span data-stu-id="b0777-133">Member has all the previous rights on the folder.</span></span>
    
<span data-ttu-id="b0777-134">frightsContact</span><span class="sxs-lookup"><span data-stu-id="b0777-134">frightsContact</span></span>
  
> <span data-ttu-id="b0777-135">Membro pode ter seu nome aparecem como o contato na pasta.</span><span class="sxs-lookup"><span data-stu-id="b0777-135">Member can have your name appear as the contact on the folder.</span></span>
    
<span data-ttu-id="b0777-136">frightsVisible</span><span class="sxs-lookup"><span data-stu-id="b0777-136">frightsVisible</span></span>
  
> <span data-ttu-id="b0777-137">Membro consegue ver a pasta existe.</span><span class="sxs-lookup"><span data-stu-id="b0777-137">Member can see that the folder exists.</span></span>
    
<span data-ttu-id="b0777-138">rightsNone</span><span class="sxs-lookup"><span data-stu-id="b0777-138">rightsNone</span></span>
  
> <span data-ttu-id="b0777-139">Membro não tem direitos na pasta.</span><span class="sxs-lookup"><span data-stu-id="b0777-139">Member does not have rights on the folder.</span></span>
    
<span data-ttu-id="b0777-140">rightsReadOnly</span><span class="sxs-lookup"><span data-stu-id="b0777-140">rightsReadOnly</span></span>
  
> <span data-ttu-id="b0777-141">Membro pode ler qualquer mensagem na pasta.</span><span class="sxs-lookup"><span data-stu-id="b0777-141">Member can read any message in the folder.</span></span>
    
<span data-ttu-id="b0777-142">rightsReadWrite</span><span class="sxs-lookup"><span data-stu-id="b0777-142">rightsReadWrite</span></span>
  
> <span data-ttu-id="b0777-143">Membro pode ler e gravar a qualquer mensagem na pasta.</span><span class="sxs-lookup"><span data-stu-id="b0777-143">Member can read from and write to any message in the folder.</span></span>
    
<span data-ttu-id="b0777-144">rightsAll</span><span class="sxs-lookup"><span data-stu-id="b0777-144">rightsAll</span></span>
  
> <span data-ttu-id="b0777-145">Membro tem todos os direitos anteriores na pasta.</span><span class="sxs-lookup"><span data-stu-id="b0777-145">Member has all the previous rights on the folder.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="b0777-146">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0777-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b0777-147">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b0777-147">Protocol specifications</span></span>

<span data-ttu-id="b0777-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0777-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0777-149">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b0777-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b0777-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0777-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0777-151">Trata as operações de pasta.</span><span class="sxs-lookup"><span data-stu-id="b0777-151">Handles folder operations.</span></span>
    
<span data-ttu-id="b0777-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0777-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0777-153">Trata a recuperação de listas de permissão de pastas que são armazenados no servidor.</span><span class="sxs-lookup"><span data-stu-id="b0777-153">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="b0777-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0777-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0777-155">Especifica os métodos para conexão e configuração de caixas de correio conforme representantes e interações com itens de mensagem e o calendário quando eles ajam em nome de outro usuário.</span><span class="sxs-lookup"><span data-stu-id="b0777-155">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b0777-156">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b0777-156">Header files</span></span>

<span data-ttu-id="b0777-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0777-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0777-158">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b0777-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="b0777-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b0777-159">Mapitags.h</span></span>
  
> <span data-ttu-id="b0777-160">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="b0777-160">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0777-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0777-161">See also</span></span>



[<span data-ttu-id="b0777-162">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0777-162">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="b0777-163">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b0777-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0777-164">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="b0777-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0777-165">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b0777-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0777-166">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b0777-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

