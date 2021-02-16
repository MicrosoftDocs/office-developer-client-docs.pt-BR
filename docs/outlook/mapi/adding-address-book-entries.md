---
title: Adicionando entradas do Livro de Endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8dc82a99ee088d42c076ca9a3a75eac6553f7d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421337"
---
# <a name="adding-address-book-entries"></a><span data-ttu-id="27085-103">Adicionando entradas do Livro de Endereços</span><span class="sxs-lookup"><span data-stu-id="27085-103">Adding Address Book Entries</span></span>

  
  
<span data-ttu-id="27085-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27085-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27085-105">Para adicionar um usuário de mensagens ou uma lista de distribuição a um contêiner, um cliente chama [IAddrBook::NewEntry](iaddrbook-newentry.md) ou um provedor chama [IMAPISupport::NewEntry](imapisupport-newentry.md) com o identificador de entrada do contêiner de destino no parâmetro _lpEIDContainer._</span><span class="sxs-lookup"><span data-stu-id="27085-105">To add a messaging user or distribution list to a container, a client calls [IAddrBook::NewEntry](iaddrbook-newentry.md) or a provider calls [IMAPISupport::NewEntry](imapisupport-newentry.md) with the entry identifier of the target container in the  _lpEIDContainer_ parameter.</span></span> <span data-ttu-id="27085-106">O MAPI, por sua vez, chama o método [IABContainer::CreateEntry](iabcontainer-createentry.md) do contêiner para criar a entrada usando um modelo único de uma tabela única.</span><span class="sxs-lookup"><span data-stu-id="27085-106">MAPI in turn calls the container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the entry using a one-off template from a one-off table.</span></span> <span data-ttu-id="27085-107">Um modelo único permite que o cliente crie um novo destinatário de um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="27085-107">A one-off template allows the client to create a new recipient of a particular type.</span></span> <span data-ttu-id="27085-108">A maioria dos campos é editável.</span><span class="sxs-lookup"><span data-stu-id="27085-108">Most of the fields are editable.</span></span> <span data-ttu-id="27085-109">O modelo apontado pelo parâmetro  _lpEntryID_ pode ser aquele que seu provedor fornece ou pode ser um modelo de um provedor estrangeiro, se seu provedor oferece suporte a modelos externos.</span><span class="sxs-lookup"><span data-stu-id="27085-109">The template pointed to by the  _lpEntryID_ parameter might be one that your provider supplies or it might be a template from a foreign provider, if your provider supports foreign templates.</span></span> <span data-ttu-id="27085-110">Implementações de **CreateEntry** para provedores que podem criar destinatários a partir de um modelo externo são sempre mais complexas do que implementações para provedores que não podem.</span><span class="sxs-lookup"><span data-stu-id="27085-110">Implementations of **CreateEntry** for providers that can create recipients from a foreign template are always more complex than implementations for providers that cannot.</span></span> 
  
 <span data-ttu-id="27085-111">**Para implementar IABContainer::CreateEntry**</span><span class="sxs-lookup"><span data-stu-id="27085-111">**To implement IABContainer::CreateEntry**</span></span>
  
1. <span data-ttu-id="27085-112">Determine o tipo de identificador de entrada especificado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="27085-112">Determine the type of entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
2. <span data-ttu-id="27085-113">Se o identificador de entrada representar um modelo para um usuário de mensagens, lista de distribuição ou contêiner de agendamento de endereço pertencente ao seu provedor:</span><span class="sxs-lookup"><span data-stu-id="27085-113">If the entry identifier represents a template for a messaging user, distribution list, or address book container owned by your provider:</span></span>
    
1. <span data-ttu-id="27085-114">Crie e inicialize o objeto apropriado.</span><span class="sxs-lookup"><span data-stu-id="27085-114">Create and initialize the appropriate object.</span></span> <span data-ttu-id="27085-115">Seu provedor pode definir algumas propriedades iniciais, se desejado.</span><span class="sxs-lookup"><span data-stu-id="27085-115">Your provider can set some initial properties if desired.</span></span> <span data-ttu-id="27085-116">Essas propriedades dependem do tipo de destinatário que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="27085-116">These properties depend on the type of recipient being created.</span></span> 
    
2. <span data-ttu-id="27085-117">Retorne um ponteiro para a implementação do objeto no conteúdo do parâmetro _lppMAPIPropEntry._</span><span class="sxs-lookup"><span data-stu-id="27085-117">Return a pointer to the object's implementation in the contents of the  _lppMAPIPropEntry_ parameter.</span></span> 
    
3. <span data-ttu-id="27085-118">Se o identificador de entrada representar um modelo para um provedor estrangeiro:</span><span class="sxs-lookup"><span data-stu-id="27085-118">If the entry identifier represents a template for a foreign provider:</span></span>
    
1. <span data-ttu-id="27085-119">Chame [IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir o objeto externo.</span><span class="sxs-lookup"><span data-stu-id="27085-119">Call [IMAPISupport::OpenEntry](imapisupport-openentry.md) to open the foreign object.</span></span> 
    
2. <span data-ttu-id="27085-120">Chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) do objeto, passando NULL para a matriz de marca de propriedade, para recuperar suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="27085-120">Call the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method, passing NULL for the property tag array, to retrieve its properties.</span></span> 
    
3. <span data-ttu-id="27085-121">Edite a matriz de valores de propriedade retornada de **GetProps** alterando a marca de propriedade para PR_NULL para todas as propriedades que não se aplicarão ao novo objeto e não devem ser transferidas.</span><span class="sxs-lookup"><span data-stu-id="27085-121">Edit the property value array returned from **GetProps** by changing the property tag to PR_NULL for all properties that will not apply to the new object and should not be transferred.</span></span> 
    
4. <span data-ttu-id="27085-122">Crie um identificador de entrada para o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="27085-122">Create an entry identifier for the new object.</span></span> 
    
5. <span data-ttu-id="27085-123">Crie um novo objeto do tipo apropriado, seja usuário de mensagens ou lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="27085-123">Create a new object of the appropriate type, either messaging user or distribution list.</span></span>
    
6. <span data-ttu-id="27085-124">Inicialize o novo objeto definindo as propriedades padrão.</span><span class="sxs-lookup"><span data-stu-id="27085-124">Initialize the new object by setting default properties.</span></span>
    
7. <span data-ttu-id="27085-125">Verifique se o objeto externo dá suporte ou não **à PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="27085-125">Check whether or not the foreign object supports the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> 
    
8. <span data-ttu-id="27085-126">Se o objeto externo suportar **PR_TEMPLATEID**, chame [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para recuperar uma interface de objeto de propriedade do provedor estrangeiro e definir o conteúdo do parâmetro  _lppMAPIPropEntry_ para a implementação de objeto de propriedade estrangeira.</span><span class="sxs-lookup"><span data-stu-id="27085-126">If the foreign object supports **PR_TEMPLATEID**, call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to retrieve a property object interface from the foreign provider and set the contents of the  _lppMAPIPropEntry_ parameter to the foreign property object implementation.</span></span> 
    
9. <span data-ttu-id="27085-127">Se o objeto externo não suportar **PR_TEMPLATEID**, de definir o conteúdo do parâmetro  _lppMAPIPropEntry_ para a implementação do novo objeto pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="27085-127">If the foreign object does not support **PR_TEMPLATEID**, set the contents of the  _lppMAPIPropEntry_ parameter to your provider's implementation of the new object.</span></span> 
    
10. <span data-ttu-id="27085-128">Chame o [método IMAPIProp::SetProps](imapiprop-setprops.md) do objeto apontado pelo parâmetro  _lppMAPIPropEntry_ para definir as propriedades apropriadas do objeto externo.</span><span class="sxs-lookup"><span data-stu-id="27085-128">Call the [IMAPIProp::SetProps](imapiprop-setprops.md) method of the object pointed to by the  _lppMAPIPropEntry_ parameter to set the appropriate properties from the foreign object.</span></span> 
    

