---
title: IABLogonOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenTemplateID
api_type:
- COM
ms.assetid: 751c36d3-c39e-4357-a60a-88685a378de0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bc68878a25873533162df7e1671e483c3bb77865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334745"
---
# <a name="iablogonopentemplateid"></a><span data-ttu-id="f566c-103">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="f566c-103">IABLogon::OpenTemplateID</span></span>

  
  
<span data-ttu-id="f566c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f566c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f566c-105">Abre uma entrada de destinatário que tem dados residindo em um provedor de agendamento de endereço de host.</span><span class="sxs-lookup"><span data-stu-id="f566c-105">Opens a recipient entry that has data residing in a host address book provider.</span></span>
  
```cpp
HRESULT OpenTemplateID(
  ULONG cbTemplateID,
  LPENTRYID lpTemplateID,
  ULONG ulTemplateFlags,
  LPMAPIPROP lpMAPIPropData,
  LPCIID lpInterface,
  LPMAPIPROP FAR * lppMAPIPropNew,
  LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a><span data-ttu-id="f566c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f566c-106">Parameters</span></span>

 <span data-ttu-id="f566c-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="f566c-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="f566c-108">[in] A contagem de byte no identificador de modelo apontado pelo parâmetro _lpTemplateID._</span><span class="sxs-lookup"><span data-stu-id="f566c-108">[in] The byte count in the template identifier pointed to by the  _lpTemplateID_ parameter.</span></span> 
    
 <span data-ttu-id="f566c-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="f566c-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="f566c-110">[in] Um ponteiro para o identificador de modelo ou **PR_TEMPLATEID** propriedade ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) da entrada do destinatário a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="f566c-110">[in] A pointer to the template identifier, or **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="f566c-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="f566c-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="f566c-112">[in] Uma bitmask de sinalizadores usada para indicar como abrir a entrada representada pelo identificador de modelo.</span><span class="sxs-lookup"><span data-stu-id="f566c-112">[in] A bitmask of flags used to indicate how to open the entry represented by the template identifier.</span></span> <span data-ttu-id="f566c-113">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="f566c-113">The following flag can be set:</span></span>
    
<span data-ttu-id="f566c-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="f566c-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="f566c-115">O provedor de host está criando uma nova entrada em seu contêiner com base na entrada representada pelo identificador do modelo.</span><span class="sxs-lookup"><span data-stu-id="f566c-115">The host provider is creating a new entry in its container based on the entry represented by the template identifier.</span></span> <span data-ttu-id="f566c-116">O método **IABLogon::OpenTemplateID** deve executar a inicialização específica da entrada do provedor host usando a implementação [IMAPIProp : IUnknown](imapipropiunknown.md) no parâmetro _lpMAPIPropData_ ou retornar uma implementação de interface **IMAPIProp** personalizada no parâmetro _lppMAPIPropNew._</span><span class="sxs-lookup"><span data-stu-id="f566c-116">The **IABLogon::OpenTemplateID** method should either perform specific initialization of the host provider's entry by using the [IMAPIProp : IUnknown](imapipropiunknown.md) implementation in the  _lpMAPIPropData_ parameter, or return a custom **IMAPIProp** interface implementation in the  _lppMAPIPropNew_ parameter.</span></span> 
    
 <span data-ttu-id="f566c-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="f566c-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="f566c-118">[in] Um ponteiro para o objeto de propriedade do provedor de host e implementação de uma interface derivada de **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="f566c-118">[in] A pointer to the host provider's property object and implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="f566c-119">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f566c-119">_lpInterface_</span></span>
  
> <span data-ttu-id="f566c-120">[in] Um ponteiro para o identificador da interface (IID) que representa o tipo de ponteiro da interface a ser retornado no parâmetro _lppMAPIPropNew._</span><span class="sxs-lookup"><span data-stu-id="f566c-120">[in] A pointer to the interface identifier (IID) that represents the type of interface pointer to be returned in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="f566c-121">Passar **nulo** retorna a interface do usuário padrão de mensagens, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="f566c-121">Passing **null** returns the standard messaging user interface, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span>
    
 <span data-ttu-id="f566c-122">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="f566c-122">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="f566c-123">[out] Um ponteiro para o objeto de propriedade vinculada e uma implementação de uma interface derivada de **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="f566c-123">[out] A pointer to the bound property object and an implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="f566c-124">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="f566c-124">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="f566c-125">[out] Reservado; deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f566c-125">[out] Reserved; must be **null**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f566c-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f566c-126">Return value</span></span>

<span data-ttu-id="f566c-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="f566c-127">S_OK</span></span> 
  
> <span data-ttu-id="f566c-128">O código apropriado foi vinculado com êxito aos dados relacionados no provedor de host.</span><span class="sxs-lookup"><span data-stu-id="f566c-128">The appropriate code was successfully bound to related data in the host provider.</span></span>
    
<span data-ttu-id="f566c-129">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f566c-129">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f566c-130">O objeto não dá suporte a IDs de modelo.</span><span class="sxs-lookup"><span data-stu-id="f566c-130">The object does not support template IDs.</span></span>
    
<span data-ttu-id="f566c-131">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f566c-131">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="f566c-132">O identificador de modelo passado no  _parâmetro lpTemplateID_ não é reconhecido pelo provedor do address book.</span><span class="sxs-lookup"><span data-stu-id="f566c-132">The template identifier passed in the  _lpTemplateID_ parameter is not recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f566c-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="f566c-133">Remarks</span></span>

<span data-ttu-id="f566c-134">O **método IABLogon::OpenTemplateID** é implementado apenas por provedores de agendamento de endereço que precisam manter o controle sobre cópias de suas entradas localizadas nos contêineres de provedores de host.</span><span class="sxs-lookup"><span data-stu-id="f566c-134">The **IABLogon::OpenTemplateID** method is implemented only by address book providers that need to maintain control over copies of their entries that are located in the containers of host providers.</span></span> <span data-ttu-id="f566c-135">Provedores que implementam **OpenTemplateID são** conhecidos como provedores de livro de endereços externos.</span><span class="sxs-lookup"><span data-stu-id="f566c-135">Providers that implement **OpenTemplateID** are known as foreign address book providers.</span></span> <span data-ttu-id="f566c-136">Provedores de host chamam [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para criar uma entrada copiada ou abrir a entrada copiada, e MAPI passa a chamada para **IABLogon::OpenTemplateID**.</span><span class="sxs-lookup"><span data-stu-id="f566c-136">Host providers call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to create a copied entry or open the copied entry, and MAPI passes on the call to **IABLogon::OpenTemplateID**.</span></span> <span data-ttu-id="f566c-137">**IABLogon::OpenTemplateID** abre a entrada e vincula o código que a controla aos dados no provedor de host.</span><span class="sxs-lookup"><span data-stu-id="f566c-137">**IABLogon::OpenTemplateID** opens the entry and binds the code that controls it to data in the host provider.</span></span> 
  
<span data-ttu-id="f566c-138">Em vez de usar um identificador de entrada, **IABLogon::OpenTemplateID** usa outra propriedade, o identificador de modelo da entrada, **PR_TEMPLATEID**.</span><span class="sxs-lookup"><span data-stu-id="f566c-138">Rather than use an entry identifier, **IABLogon::OpenTemplateID** uses another property, the entry's template identifier, **PR_TEMPLATEID**.</span></span> <span data-ttu-id="f566c-139">Os identificadores de modelo devem ter suporte para entradas cujo código deve ser vinculado aos dados em um provedor de host.</span><span class="sxs-lookup"><span data-stu-id="f566c-139">Template identifiers should be supported for entries whose code must be bound to data in a host provider.</span></span>
  
<span data-ttu-id="f566c-140">Alguns exemplos de quando um provedor de agendamento de endereços deve implementar **IABLogon::OpenTemplateID** são:</span><span class="sxs-lookup"><span data-stu-id="f566c-140">Some examples of when an address book provider should implement **IABLogon::OpenTemplateID** are as follows:</span></span> 
  
- <span data-ttu-id="f566c-141">Para atualizar periodicamente os dados de uma entrada copiada para que permaneçam sincronizados com o original.</span><span class="sxs-lookup"><span data-stu-id="f566c-141">To periodically update the data for a copied entry so that it stays synchronized with the original.</span></span>
    
- <span data-ttu-id="f566c-142">Para implementar a funcionalidade que o provedor de host não pode implementar, como preencher dinamicamente uma lista que aparece na tabela de detalhes da entrada de dados em um servidor.</span><span class="sxs-lookup"><span data-stu-id="f566c-142">To implement functionality that the host provider cannot implement, such as dynamically populating a list that appears in the entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="f566c-143">Para controlar a interação entre as propriedades na entrada do provedor host e a entrada original, como calcular o **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) dos valores dos controles de edição na exibição de detalhes que contêm diferentes componentes do endereço.</span><span class="sxs-lookup"><span data-stu-id="f566c-143">To control the interaction between properties in the host provider's entry and the original entry, such as computing the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) from the values of the edit controls in the details display that contain different components of the address.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="f566c-144">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="f566c-144">Notes to implementers</span></span>

<span data-ttu-id="f566c-145">Quando um provedor de host copia ou cria uma entrada de seu provedor e você fornece uma implementação de objeto de propriedade por meio de **IABLogon::OpenTemplateID**, você lida com a maioria das chamadas para manter a entrada.</span><span class="sxs-lookup"><span data-stu-id="f566c-145">When a host provider copies or creates an entry from your provider and you supply a property object implementation through **IABLogon::OpenTemplateID**, you handle most of the calls to maintain the entry.</span></span> <span data-ttu-id="f566c-146">No entanto, como o provedor de host deve encaminhar essas chamadas para você, o provedor de host pode interceptar qualquer chamada e executar o processamento personalizado antes de encaminhar a chamada.</span><span class="sxs-lookup"><span data-stu-id="f566c-146">However, because it is up to the host provider to forward these calls to you, the host provider can intercept any call and perform custom processing before forwarding the call.</span></span>
  
<span data-ttu-id="f566c-147">Você deve usar as seguintes diretrizes em suas implementações de objeto de propriedade:</span><span class="sxs-lookup"><span data-stu-id="f566c-147">You should use the following guidelines in your property object implementations:</span></span>
  
- <span data-ttu-id="f566c-148">Quando [IMAPIProp::GetProps](imapiprop-getprops.md) for chamado, determine se a solicitação é para uma propriedade computada e, se for, lidar com ela.</span><span class="sxs-lookup"><span data-stu-id="f566c-148">When [IMAPIProp::GetProps](imapiprop-getprops.md) is called, determine whether the request is for a computed property and, if it is, handle it.</span></span> <span data-ttu-id="f566c-149">Transfira todas as solicitações de propriedades nãocomputadas para o provedor de host.</span><span class="sxs-lookup"><span data-stu-id="f566c-149">Transfer all requests for noncomputed properties to the host provider.</span></span> 
    
- <span data-ttu-id="f566c-150">Quando [IMAPIProp::OpenProperty](imapiprop-openproperty.md) é chamado para abrir qualquer tabela, exceto a tabela de exibição de detalhes, manipular a solicitação.</span><span class="sxs-lookup"><span data-stu-id="f566c-150">When [IMAPIProp::OpenProperty](imapiprop-openproperty.md) is called to open any table except the details display table, handle the request.</span></span> <span data-ttu-id="f566c-151">A maioria das tabelas não pode ser copiada com precisão para o provedor de host.</span><span class="sxs-lookup"><span data-stu-id="f566c-151">Most tables cannot be copied accurately to the host provider.</span></span> <span data-ttu-id="f566c-152">Você deve gerar a **implementação IMAPITable** para essas tabelas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="f566c-152">You must generate the **IMAPITable** implementation for these requested tables.</span></span> <span data-ttu-id="f566c-153">A tabela de **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) deve ser copiada para o provedor de host.</span><span class="sxs-lookup"><span data-stu-id="f566c-153">The details table **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property must be copied to the host provider.</span></span> <span data-ttu-id="f566c-154">Isso permite que esse provedor gere a tabela localmente.</span><span class="sxs-lookup"><span data-stu-id="f566c-154">This allows this provider to generate the table locally.</span></span> <span data-ttu-id="f566c-155">Talvez você queira quebrar a implementação da tabela de exibição para gerar notificações de tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="f566c-155">You might want to wrap the display table implementation to generate display table notifications.</span></span> 
    
- <span data-ttu-id="f566c-156">Quando [IMAPIProp::SetProps](imapiprop-setprops.md) é chamado, o provedor de host pode validar os dados antes de permitir a definição das propriedades.</span><span class="sxs-lookup"><span data-stu-id="f566c-156">When [IMAPIProp::SetProps](imapiprop-setprops.md) is called, the host provider can validate the data before letting you set the properties.</span></span> <span data-ttu-id="f566c-157">Você pode verificar se todas as propriedades necessárias foram definidas ou computadas.</span><span class="sxs-lookup"><span data-stu-id="f566c-157">You can verify that all of the necessary properties were set or computed.</span></span> <span data-ttu-id="f566c-158">Se um erro for detectado, retorne o valor de erro apropriado e, se possível, qualquer explicação adicional por meio de [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="f566c-158">If an error is detected, return the appropriate error value and, if you can, any additional explanation through [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span>
    
- <span data-ttu-id="f566c-159">Quando [IMAPIProp::SaveChanges](imapiprop-savechanges.md) é chamado, o provedor host pode querer executar o processamento antes de salvar a entrada.</span><span class="sxs-lookup"><span data-stu-id="f566c-159">When [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called, the host provider might want to perform processing before you save the entry.</span></span> <span data-ttu-id="f566c-160">Você deve salvar quaisquer dados afetados pelas propriedades alteradas, como um novo endereço, na entrada do provedor de host.</span><span class="sxs-lookup"><span data-stu-id="f566c-160">You should save any data that is affected by the changed properties, such as a new address, in the host provider's entry.</span></span> 
    
<span data-ttu-id="f566c-161">Em geral, faça sua implementação da entrada que você passa de volta para o provedor host interceptar todos os métodos para executar manipulação específica de contexto das propriedades relevantes.</span><span class="sxs-lookup"><span data-stu-id="f566c-161">In general, make your implementation of the entry that you pass back to the host provider intercept all of the methods to perform context-specific manipulation of the relevant properties.</span></span> <span data-ttu-id="f566c-162">Se o FILL_ENTRY sinalizador for passado no  _parâmetro ulTemplateFlags,_ defina todas as propriedades para a entrada.</span><span class="sxs-lookup"><span data-stu-id="f566c-162">If the FILL_ENTRY flag is passed in the  _ulTemplateFlags_ parameter, set all properties for the entry.</span></span> 
  
<span data-ttu-id="f566c-163">Se você retornar um novo objeto de propriedade no parâmetro  _lppMAPIPropNew,_ chame o método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) do objeto de propriedade do provedor de host para manter uma referência.</span><span class="sxs-lookup"><span data-stu-id="f566c-163">If you return a new property object in the  _lppMAPIPropNew_ parameter, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method of the host provider's property object to maintain a reference.</span></span> <span data-ttu-id="f566c-164">Todas as chamadas através do objeto vinculado que a implementação **de IMAPIProp** retornada em  _lppMAPIPropNew_ devem ser roteadas para o método correspondente no objeto de propriedade host depois que eles são tratados pelo objeto vinculado.</span><span class="sxs-lookup"><span data-stu-id="f566c-164">All calls through the bound object that the **IMAPIProp** implementation returned in  _lppMAPIPropNew_ should be routed to their corresponding method in the host property object after they are dealt with by the bound object.</span></span> 
  
<span data-ttu-id="f566c-165">Os identificadores de propriedade de quaisquer propriedades nomeadas que são passadas pelo objeto de propriedade vinculada estão no namespace do identificador do provedor.</span><span class="sxs-lookup"><span data-stu-id="f566c-165">The property identifiers of any named properties that are passed through your bound property object are in your provider's identifier namespace.</span></span> <span data-ttu-id="f566c-166">Sua implementação do [método IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) deve determinar os nomes das propriedades para que ele possa executar qualquer tarefa específica do modelo.</span><span class="sxs-lookup"><span data-stu-id="f566c-166">Your implementation of the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method should determine the names of the properties so that it can perform any template-specific tasks.</span></span> <span data-ttu-id="f566c-167">Da mesma forma, as propriedades que seu provedor passa para o provedor de host também devem estar em seu namespace.</span><span class="sxs-lookup"><span data-stu-id="f566c-167">Similarly, properties that your provider passes on to the host provider must also be in your namespace.</span></span> <span data-ttu-id="f566c-168">Por exemplo, se você definir uma propriedade nomeada em **OpenTemplateID**, deverá usar um de seus identificadores para o nome criando-a, se necessário, chamando o método [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="f566c-168">For example, if you set a named property in **OpenTemplateID**, you should use one of your identifiers for the name—creating it, if necessary, by calling the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="f566c-169">Se você não reconhecer o identificador de entrada passado  _em lpTemplateID,_ retorne MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="f566c-169">If you do not recognize the entry identifier passed in  _lpTemplateID_, return MAPI_E_UNKNOWN_ENTRYID.</span></span>
  
<span data-ttu-id="f566c-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f566c-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f566c-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="f566c-171">See also</span></span>



[<span data-ttu-id="f566c-172">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="f566c-172">IMAPISupport::OpenTemplateID</span></span>](imapisupport-opentemplateid.md)
  
[<span data-ttu-id="f566c-173">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f566c-173">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="f566c-174">Propriedade canônica PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="f566c-174">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="f566c-175">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f566c-175">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

