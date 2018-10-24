---
title: IABLogonPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.PrepareRecips
api_type:
- COM
ms.assetid: 3c1845ea-e291-4855-9afd-51d2c64d7e85
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c42077528a4f7227321d8f987cc5dd0ccd4c966c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589739"
---
# <a name="iablogonpreparerecips"></a><span data-ttu-id="dfc21-103">IABLogon::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="dfc21-103">IABLogon::PrepareRecips</span></span>

<span data-ttu-id="dfc21-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfc21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfc21-105">Prepara uma lista de destinatários para uso posterior pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dfc21-105">Prepares a recipient list for later use by the messaging system.</span></span>
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="dfc21-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfc21-106">Parameters</span></span>

<span data-ttu-id="dfc21-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dfc21-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dfc21-108">[in] Uma bitmask dos sinalizadores que controla o tipo do texto em cadeias de caracteres retornadas.</span><span class="sxs-lookup"><span data-stu-id="dfc21-108">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="dfc21-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="dfc21-109">The following flag can be set:</span></span>
    
  - <span data-ttu-id="dfc21-110">MAPI_CACHE_ONLY: Use somente o catálogo de endereços offline para executar a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="dfc21-110">MAPI_CACHE_ONLY: Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="dfc21-111">Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente para abrir a lista de endereços global (GAL) no modo cache do exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="dfc21-111">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="dfc21-112">Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.</span><span class="sxs-lookup"><span data-stu-id="dfc21-112">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="dfc21-113">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="dfc21-113">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="dfc21-114">[in] Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade que indicam as propriedades que requeiram a atualização, se houver alguma.</span><span class="sxs-lookup"><span data-stu-id="dfc21-114">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties that require updating, if any.</span></span> <span data-ttu-id="dfc21-115">O parâmetro _lpPropTagArray_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="dfc21-115">The  _lpPropTagArray_ parameter can be NULL.</span></span> 
    
<span data-ttu-id="dfc21-116">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="dfc21-116">_lpRecipList_</span></span>
  
> <span data-ttu-id="dfc21-117">[in] Um ponteiro para uma estrutura [ADRLIST](adrlist.md) que contém a lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="dfc21-117">[in] A pointer to an [ADRLIST](adrlist.md) structure that holds the recipient list.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dfc21-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dfc21-118">Return value</span></span>

<span data-ttu-id="dfc21-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="dfc21-119">S_OK</span></span> 
  
> <span data-ttu-id="dfc21-120">A lista de destinatários foi preparada com êxito.</span><span class="sxs-lookup"><span data-stu-id="dfc21-120">The recipient list was successfully prepared.</span></span>
    
<span data-ttu-id="dfc21-121">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="dfc21-121">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="dfc21-122">Um ou mais dos destinatários no parâmetro _lpRecipList_ não existem.</span><span class="sxs-lookup"><span data-stu-id="dfc21-122">One or more of the recipients in the  _lpRecipList_ parameter do not exist.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dfc21-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dfc21-123">Return value</span></span>

<span data-ttu-id="dfc21-124">Um cliente chama o método MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) para modificar ou reorganizar um conjunto de propriedades para um ou mais destinatários.</span><span class="sxs-lookup"><span data-stu-id="dfc21-124">A client calls the MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method to modify or rearrange a set of properties for one or more recipients.</span></span> <span data-ttu-id="dfc21-125">Os destinatários podem ou não podem ser a parte da lista de destinatários de uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="dfc21-125">The recipients may or may not be part of the recipient list of an outgoing message.</span></span> <span data-ttu-id="dfc21-126">MAPI transfere essa chamada para o método de **IABLogon::PrepareRecips** de um provedor catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="dfc21-126">MAPI transfers this call to an address book provider's **IABLogon::PrepareRecips** method.</span></span> 
  
<span data-ttu-id="dfc21-127">**IABLogon::PrepareRecips** executa as quatro tarefas principais:</span><span class="sxs-lookup"><span data-stu-id="dfc21-127">**IABLogon::PrepareRecips** performs four main tasks:</span></span> 
  
- <span data-ttu-id="dfc21-128">Garante que todos os destinatários na lista de endereços apontadas pelo parâmetro _lpRecipList_ tiver um identificador de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="dfc21-128">Ensures that all recipients in the address list pointed to by the  _lpRecipList_ parameter have a long-term entry identifier.</span></span> 
    
- <span data-ttu-id="dfc21-129">Garante que todos os destinatários tenham as propriedades especificadas na matriz de valores de propriedade apontado pelo parâmetro _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="dfc21-129">Ensures that all recipients have the properties specified in the property value array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
    
- <span data-ttu-id="dfc21-130">Garante que as propriedades da matriz de valores de propriedade aparecem antes de quaisquer outras propriedades que se encontrava antes da chamada.</span><span class="sxs-lookup"><span data-stu-id="dfc21-130">Ensures that the properties from the property value array appear before any other properties that existed before the call.</span></span>
    
- <span data-ttu-id="dfc21-131">Garante que a ordem das propriedades na estrutura [ADRENTRY](adrentry.md) de cada destinatário na estrutura de **ADRLIST** é o mesmo que a matriz de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="dfc21-131">Ensures that the order of the properties in each recipient's [ADRENTRY](adrentry.md) structure in the **ADRLIST** structure is the same as in the property value array.</span></span> 
    
<span data-ttu-id="dfc21-132">A estrutura **ADRENTRY** no parâmetro _lpRecipList_ contém uma estrutura **ADRENTRY** para cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="dfc21-132">The **ADRENTRY** structure in the  _lpRecipList_ parameter contains one **ADRENTRY** structure for each recipient.</span></span> <span data-ttu-id="dfc21-133">Cada estrutura **ADRENTRY** contém uma matriz de estruturas [SPropValue](spropvalue.md) para descrever as propriedades do destinatário.</span><span class="sxs-lookup"><span data-stu-id="dfc21-133">Each **ADRENTRY** structure contains an array of [SPropValue](spropvalue.md) structures to describe the recipient's properties.</span></span> <span data-ttu-id="dfc21-134">Quando **IABLogon::PrepareRecips** retorna, a matriz de estrutura de **SPropValue** para cada destinatário inclui as propriedades de _lpPropTagArray_ seguido as outras propriedades para o destinatário.</span><span class="sxs-lookup"><span data-stu-id="dfc21-134">When **IABLogon::PrepareRecips** returns, the **SPropValue** structure array for each recipient includes the properties from the  _lpPropTagArray_ followed by the other properties for the recipient.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="dfc21-135">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="dfc21-135">Notes to implementers</span></span>

<span data-ttu-id="dfc21-136">Implementar **IABLogon::PrepareRecips** envolve a colocação de propriedades em uma ordem específica, recuperando valores de propriedade e conversão de curto prazo identificadores de entrada aos identificadores de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="dfc21-136">Implementing **IABLogon::PrepareRecips** involves putting properties in a specific order, retrieving property values, and converting short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="dfc21-137">As propriedades que são solicitadas no parâmetro _lpPropTagArray_ devem ser no início da matriz de valores de propriedade associado a estrutura **ADRENTRY** de cada destinatário no parâmetro _lpRecipList_ .</span><span class="sxs-lookup"><span data-stu-id="dfc21-137">The properties that are requested in the  _lpPropTagArray_ parameter must be at the start of the property value array associated with each recipient's **ADRENTRY** structure in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="dfc21-138">Se os valores dessas propriedades não existirem, abra a lista de distribuição ou usuário mensagens associada usando seu identificador de entrada e recuperar os valores de propriedade ausente.</span><span class="sxs-lookup"><span data-stu-id="dfc21-138">If values for these properties do not exist, open the associated messaging user or distribution list by using its entry identifier and retrieve the missing property values.</span></span> 
  
<span data-ttu-id="dfc21-139">Aloca cada estrutura **SPropValue** passada na _lpRecipList_ separadamente para que as estruturas podem ser liberadas individualmente.</span><span class="sxs-lookup"><span data-stu-id="dfc21-139">Allocate each **SPropValue** structure passed in  _lpRecipList_ separately so that the structures can be freed individually.</span></span> <span data-ttu-id="dfc21-140">Se você deve alocar espaço adicional para qualquer estrutura **SPropValue** , por exemplo, para armazenar os dados para uma propriedade de cadeia de caracteres, use a função [MAPIAllocateBuffer](mapiallocatebuffer.md) para alocar espaço adicional para a matriz de valor de propriedade completo.</span><span class="sxs-lookup"><span data-stu-id="dfc21-140">If you must allocate additional space for any **SPropValue** structure, for example, to store the data for a string property, use the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate additional space for the full property value array.</span></span> <span data-ttu-id="dfc21-141">Use a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar a matriz de valores de propriedade original e, em seguida, use a função de [MAPIAllocateMore](mapiallocatemore.md) para alocar toda a memória adicional que é necessária.</span><span class="sxs-lookup"><span data-stu-id="dfc21-141">Use the [MAPIFreeBuffer](mapifreebuffer.md) function to free the original property value array, and then use the [MAPIAllocateMore](mapiallocatemore.md) function to allocate any additional memory that is required.</span></span> 
  
<span data-ttu-id="dfc21-142">Para implementar **IABLogon::PrepareRecips**, use o procedimento a seguir:</span><span class="sxs-lookup"><span data-stu-id="dfc21-142">To implement **IABLogon::PrepareRecips**, use the following procedure:</span></span>
  
1. <span data-ttu-id="dfc21-143">Verifique se há entradas no parâmetro _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="dfc21-143">Check for entries in the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="dfc21-144">Se a matriz de valores de propriedade estiver vazia, não há nenhum trabalho a ser feito.</span><span class="sxs-lookup"><span data-stu-id="dfc21-144">If the property value array is empty, there is no work to do.</span></span> <span data-ttu-id="dfc21-145">Retorna um valor de sucesso.</span><span class="sxs-lookup"><span data-stu-id="dfc21-145">Return a success value.</span></span> 
    
2. <span data-ttu-id="dfc21-146">Processo de cada destinatário no parâmetro _lpRecipList_ .</span><span class="sxs-lookup"><span data-stu-id="dfc21-146">Process each recipient in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="dfc21-147">Não há um membro de estrutura **ADRENTRY** para cada destinatário na lista.</span><span class="sxs-lookup"><span data-stu-id="dfc21-147">There is one **ADRENTRY** structure member for each recipient in the list.</span></span> <span data-ttu-id="dfc21-148">Ignore os seguintes tipos de destinatários:</span><span class="sxs-lookup"><span data-stu-id="dfc21-148">Ignore the following types of recipients:</span></span> 
    
   - <span data-ttu-id="dfc21-149">Destinatários sem um identificador de entrada no membro **rgPropVals** da sua estrutura **ADRENTRY** (ou seja, os destinatários não resolvidos).</span><span class="sxs-lookup"><span data-stu-id="dfc21-149">Recipients without an entry identifier in the **rgPropVals** member of their **ADRENTRY** structure (that is, unresolved recipients).</span></span> 
    
   - <span data-ttu-id="dfc21-150">Destinatários com um identificador de entrada que não pertencem ao provedor.</span><span class="sxs-lookup"><span data-stu-id="dfc21-150">Recipients with an entry identifier that does not belong to your provider.</span></span> <span data-ttu-id="dfc21-151">Esses destinatários serão transmitidos ao outro provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="dfc21-151">These recipients will be passed to another address book provider.</span></span>
    
3. <span data-ttu-id="dfc21-152">Abra o destinatário e recuperar as propriedades que já estão definidas para o destinatário.</span><span class="sxs-lookup"><span data-stu-id="dfc21-152">Open the recipient and retrieve the properties that are already set for the recipient.</span></span>
    
4. <span data-ttu-id="dfc21-153">Mescle a matriz de valores de propriedade especificado no _lpRecipList_ com a matriz de propriedades retornado da **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="dfc21-153">Merge the property value array specified in the  _lpRecipList_ with the array of properties returned from **GetProps**.</span></span> <span data-ttu-id="dfc21-154">Se a mesma propriedade ocorre em ambas as matrizes de propriedade, use o valor de _lpRecipList_.</span><span class="sxs-lookup"><span data-stu-id="dfc21-154">If the same property occurs in both property arrays, use the value from  _lpRecipList_.</span></span>
    
5. <span data-ttu-id="dfc21-155">Se a matriz de valores de propriedade _lpRecipList_ é grande o suficiente para armazenar todas as propriedades necessárias, simplesmente substitua-la com a matriz mesclada.</span><span class="sxs-lookup"><span data-stu-id="dfc21-155">If the  _lpRecipList_ property value array is big enough to hold all of the necessary properties, just replace it with the merged array.</span></span> <span data-ttu-id="dfc21-156">Se a matriz de valor de propriedade _lpRecipList_ não é grande o suficiente, substitua-o com uma matriz alocada recentemente.</span><span class="sxs-lookup"><span data-stu-id="dfc21-156">If the  _lpRecipList_ property value array is not big enough, replace it with a newly allocated array.</span></span> <span data-ttu-id="dfc21-157">Certifique-se de que a nova matriz tem um valor atualizado em cada um dos seus membros **cValues** .</span><span class="sxs-lookup"><span data-stu-id="dfc21-157">Be sure the new array has an updated value in each of its **cValues** members.</span></span> 
    
6. <span data-ttu-id="dfc21-158">Se você não reconhecer uma ou mais das propriedades no parâmetro _lpPropTagArray_ , definir o tipo de propriedade na estrutura **ADRENTRY** do destinatário PT_ERROR e o valor da propriedade para E_NOT_FOUND ou para outro valor que oferece uma mais motivo específico de indisponibilidade da propriedade.</span><span class="sxs-lookup"><span data-stu-id="dfc21-158">If you do not recognize one or more of the properties in the  _lpPropTagArray_ parameter, set the property type in the recipient's **ADRENTRY** structure to PT_ERROR and the property value either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason for the unavailability of the property.</span></span> <span data-ttu-id="dfc21-159">Para obter informações sobre PT_ERROR, consulte [Tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="dfc21-159">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="dfc21-160">Nunca realocar a estrutura **ADRLIST** que é passada para **IABLogon::PrepareRecips** ou alterar seu número de entradas.</span><span class="sxs-lookup"><span data-stu-id="dfc21-160">Never reallocate the **ADRLIST** structure that is passed into **IABLogon::PrepareRecips** or change its number of entries.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dfc21-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfc21-161">See also</span></span>

- [<span data-ttu-id="dfc21-162">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="dfc21-162">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="dfc21-163">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="dfc21-163">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="dfc21-164">Propriedade canônico PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="dfc21-164">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
- [<span data-ttu-id="dfc21-165">SPropValue</span><span class="sxs-lookup"><span data-stu-id="dfc21-165">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="dfc21-166">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dfc21-166">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

