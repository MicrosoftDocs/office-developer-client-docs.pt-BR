---
title: Adicionar entradas ao catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d5b2aa2830e2721b9f895b22df12c9d712188625
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590131"
---
# <a name="adding-address-book-entries"></a><span data-ttu-id="7e163-103">Adicionar entradas ao catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="7e163-103">Adding Address Book Entries</span></span>

  
  
<span data-ttu-id="7e163-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e163-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e163-105">Para adicionar um usuário de mensagens ou a lista de distribuição para um contêiner, a chamadas de cliente [IAddrBook::NewEntry](iaddrbook-newentry.md) ou um provedor chama [IMAPISupport::NewEntry](imapisupport-newentry.md) com o identificador de entrada do contêiner de destino no parâmetro _lpEIDContainer_ .</span><span class="sxs-lookup"><span data-stu-id="7e163-105">To add a messaging user or distribution list to a container, a client calls [IAddrBook::NewEntry](iaddrbook-newentry.md) or a provider calls [IMAPISupport::NewEntry](imapisupport-newentry.md) with the entry identifier of the target container in the  _lpEIDContainer_ parameter.</span></span> <span data-ttu-id="7e163-106">MAPI por sua vez chama o método de [IABContainer::CreateEntry](iabcontainer-createentry.md) do contêiner para criar a entrada usando um modelo único de uma tabela único.</span><span class="sxs-lookup"><span data-stu-id="7e163-106">MAPI in turn calls the container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the entry using a one-off template from a one-off table.</span></span> <span data-ttu-id="7e163-107">Um modelo único permite que o cliente criar um novo destinatário de um determinado tipo.</span><span class="sxs-lookup"><span data-stu-id="7e163-107">A one-off template allows the client to create a new recipient of a particular type.</span></span> <span data-ttu-id="7e163-108">A maioria dos campos podem ser editada.</span><span class="sxs-lookup"><span data-stu-id="7e163-108">Most of the fields are editable.</span></span> <span data-ttu-id="7e163-109">O modelo apontado pelo parâmetro _lpEntryID_ pode ser uma que seu provedor fornece ou talvez seja um modelo de um provedor estrangeiro, se o provedor oferece suporte a modelos estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="7e163-109">The template pointed to by the  _lpEntryID_ parameter might be one that your provider supplies or it might be a template from a foreign provider, if your provider supports foreign templates.</span></span> <span data-ttu-id="7e163-110">Implementações de **CreateEntry** para provedores que podem criar destinatários a partir de um modelo estrangeiro sempre são mais complexos que implementações para provedores que não é possível.</span><span class="sxs-lookup"><span data-stu-id="7e163-110">Implementations of **CreateEntry** for providers that can create recipients from a foreign template are always more complex than implementations for providers that cannot.</span></span> 
  
 <span data-ttu-id="7e163-111">**Para implementar IABContainer::CreateEntry**</span><span class="sxs-lookup"><span data-stu-id="7e163-111">**To implement IABContainer::CreateEntry**</span></span>
  
1. <span data-ttu-id="7e163-112">Determine o tipo de identificador de entrada especificada pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="7e163-112">Determine the type of entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
2. <span data-ttu-id="7e163-113">Se o identificador de entrada representa um modelo para um usuário de mensagens, lista de distribuição ou pertencentes ao seu provedor de contêiner de catálogo de endereços:</span><span class="sxs-lookup"><span data-stu-id="7e163-113">If the entry identifier represents a template for a messaging user, distribution list, or address book container owned by your provider:</span></span>
    
1. <span data-ttu-id="7e163-114">Criar e inicializar o objeto apropriado.</span><span class="sxs-lookup"><span data-stu-id="7e163-114">Create and initialize the appropriate object.</span></span> <span data-ttu-id="7e163-115">Seu provedor pode definir algumas propriedades iniciais, se desejado.</span><span class="sxs-lookup"><span data-stu-id="7e163-115">Your provider can set some initial properties if desired.</span></span> <span data-ttu-id="7e163-116">Essas propriedades dependem do tipo de destinatário que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="7e163-116">These properties depend on the type of recipient being created.</span></span> 
    
2. <span data-ttu-id="7e163-117">Retorne um ponteiro para a implementação do objeto, no conteúdo do parâmetro _lppMAPIPropEntry_ .</span><span class="sxs-lookup"><span data-stu-id="7e163-117">Return a pointer to the object's implementation in the contents of the  _lppMAPIPropEntry_ parameter.</span></span> 
    
3. <span data-ttu-id="7e163-118">Se o identificador de entrada representa um modelo para um provedor de externo:</span><span class="sxs-lookup"><span data-stu-id="7e163-118">If the entry identifier represents a template for a foreign provider:</span></span>
    
1. <span data-ttu-id="7e163-119">Chame [IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir o objeto estranho.</span><span class="sxs-lookup"><span data-stu-id="7e163-119">Call [IMAPISupport::OpenEntry](imapisupport-openentry.md) to open the foreign object.</span></span> 
    
2. <span data-ttu-id="7e163-120">Chame o método do objeto [IMAPIProp::GetProps](imapiprop-getprops.md) , passando NULL para a matriz de marca de propriedade, para recuperar as suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7e163-120">Call the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method, passing NULL for the property tag array, to retrieve its properties.</span></span> 
    
3. <span data-ttu-id="7e163-121">Edite a matriz de valores de propriedade retornado de **GetProps** , alterando a marca de propriedade para PR_NULL para todas as propriedades que não serão aplicadas ao novo objeto e não devem ser transferidas.</span><span class="sxs-lookup"><span data-stu-id="7e163-121">Edit the property value array returned from **GetProps** by changing the property tag to PR_NULL for all properties that will not apply to the new object and should not be transferred.</span></span> 
    
4. <span data-ttu-id="7e163-122">Crie um identificador de entrada para o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="7e163-122">Create an entry identifier for the new object.</span></span> 
    
5. <span data-ttu-id="7e163-123">Criar um novo objeto de apropriada, digite qualquer lista de usuário ou de distribuição de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7e163-123">Create a new object of the appropriate type, either messaging user or distribution list.</span></span>
    
6. <span data-ttu-id="7e163-124">Inicialize o novo objeto, definindo as propriedades padrão.</span><span class="sxs-lookup"><span data-stu-id="7e163-124">Initialize the new object by setting default properties.</span></span>
    
7. <span data-ttu-id="7e163-125">Verifique se ou não um objeto estranho suporta a propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7e163-125">Check whether or not the foreign object supports the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> 
    
8. <span data-ttu-id="7e163-126">Se o objeto estranho suporta **PR_TEMPLATEID**, chame [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para recuperar uma interface de objeto de propriedade do provedor de estrangeira e definir o conteúdo do parâmetro _lppMAPIPropEntry_ para a propriedade foreign implementação de objeto.</span><span class="sxs-lookup"><span data-stu-id="7e163-126">If the foreign object supports **PR_TEMPLATEID**, call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to retrieve a property object interface from the foreign provider and set the contents of the  _lppMAPIPropEntry_ parameter to the foreign property object implementation.</span></span> 
    
9. <span data-ttu-id="7e163-127">Se o objeto estranho não oferece suporte a **PR_TEMPLATEID**, defina o conteúdo do parâmetro _lppMAPIPropEntry_ a implementação do seu provedor do novo objeto.</span><span class="sxs-lookup"><span data-stu-id="7e163-127">If the foreign object does not support **PR_TEMPLATEID**, set the contents of the  _lppMAPIPropEntry_ parameter to your provider's implementation of the new object.</span></span> 
    
10. <span data-ttu-id="7e163-128">Chame o método [IMAPIProp::SetProps](imapiprop-setprops.md) do objeto apontado pelo parâmetro _lppMAPIPropEntry_ para definir as propriedades adequadas de um objeto estranho.</span><span class="sxs-lookup"><span data-stu-id="7e163-128">Call the [IMAPIProp::SetProps](imapiprop-setprops.md) method of the object pointed to by the  _lppMAPIPropEntry_ parameter to set the appropriate properties from the foreign object.</span></span> 
    

