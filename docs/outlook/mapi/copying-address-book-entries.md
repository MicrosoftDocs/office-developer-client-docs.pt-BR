---
title: Copiar entradas do catálogo de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 190c4bf12c8f5aaaf8143f59239bb53fb68046f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333065"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="d00d9-103">Copiar entradas do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="d00d9-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="d00d9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d00d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d00d9-105">O método [IABContainer:: CopyEntries](iabcontainer-copyentries.md) do seu contêiner é chamado quando um ou mais destinatários do mesmo ou de outro contêiner devem ser copiados para esse contêiner.</span><span class="sxs-lookup"><span data-stu-id="d00d9-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="d00d9-106">O **CopyEntries** tem quatro parâmetros de entrada: uma matriz de identificadores de entrada que representa os destinatários a serem copiados, um identificador de janela para o indicador de progresso, um ponteiro de objeto Progress e um valor flags.</span><span class="sxs-lookup"><span data-stu-id="d00d9-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="d00d9-107">Seu provedor deve exibir o progresso se o sinalizador AB_NO_DIALOG não estiver definido e usar o objeto Progress do parâmetro _lpProgress_ , se não for NULL.</span><span class="sxs-lookup"><span data-stu-id="d00d9-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="d00d9-108">Se _lpProgress_ for NULL, chame [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) para usar o objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="d00d9-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="d00d9-109">Para obter mais informações sobre como exibir o progresso, consulte [exibindo um indicador de progresso](mapi-progress-indicators.md).</span><span class="sxs-lookup"><span data-stu-id="d00d9-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="d00d9-110">Além de AB_NO_DIALOG para suprimir um indicador de progresso, um dos dois outros sinalizadores pode ser definido para solicitar um tipo de verificação de entrada duplicada: CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT.</span><span class="sxs-lookup"><span data-stu-id="d00d9-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="d00d9-111">Os sinalizadores CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT são apenas sugestões de como o provedor determina entradas duplicadas e pode ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="d00d9-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="d00d9-112">MAPI sugere que seu provedor implemente suporte para esses sinalizadores da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="d00d9-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="d00d9-113">**Sinalizador de entrada duplicado**</span><span class="sxs-lookup"><span data-stu-id="d00d9-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="d00d9-114">**Implementação sugerida**</span><span class="sxs-lookup"><span data-stu-id="d00d9-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d00d9-115">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="d00d9-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="d00d9-116">Verifique se o nome de exibição na entrada a ser criada corresponde ao nome de exibição de uma entrada que já está no contêiner.</span><span class="sxs-lookup"><span data-stu-id="d00d9-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="d00d9-117">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="d00d9-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="d00d9-118">Verifique se o nome de exibição e a chave de pesquisa na entrada a ser criada correspondem ao nome de exibição e à chave de pesquisa de uma entrada de contêiner.</span><span class="sxs-lookup"><span data-stu-id="d00d9-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="d00d9-119">O último sinalizador, CREATE_REPLACE, indica que a nova entrada deve substituir a existente se o seu provedor tiver determinado que uma entrada a ser criada é uma duplicata de uma entrada que já está no seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="d00d9-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="d00d9-120">Se seu provedor for um catálogo de endereços pessoal, inclua a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) em cada operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="d00d9-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="d00d9-121">Incluir a tabela detalhes de exibição de um destinatário copiado permite que seu contêiner exiba os detalhes do destinatário em vez de ter que chamar o contêiner original para criar a exibição.</span><span class="sxs-lookup"><span data-stu-id="d00d9-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="d00d9-122">**Para implementar o IABContainer:: CopyEntries**</span><span class="sxs-lookup"><span data-stu-id="d00d9-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="d00d9-123">Determine se cada identificador de entrada no parâmetro _lpEntries_ está em um formato que seu provedor manipula e, se não for, falhará e retornará MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="d00d9-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="d00d9-124">Se um identificador de entrada representar um usuário de mensagens, uma lista de distribuição ou um contêiner que seu provedor manipular:</span><span class="sxs-lookup"><span data-stu-id="d00d9-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="d00d9-125">Chame o método [IMAPISupport:: OpenEntry](imapisupport-openentry.md) para abrir o destinatário correspondente.</span><span class="sxs-lookup"><span data-stu-id="d00d9-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="d00d9-126">Copie o destinatário para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="d00d9-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="d00d9-127">Se o identificador de entrada representar um destinatário estrangeiro:</span><span class="sxs-lookup"><span data-stu-id="d00d9-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="d00d9-128">Chame o método [IABContainer:: createentry](iabcontainer-createentry.md) do seu contêiner para criar um novo destinatário.</span><span class="sxs-lookup"><span data-stu-id="d00d9-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="d00d9-129">Definir propriedades iniciais no novo destinatário.</span><span class="sxs-lookup"><span data-stu-id="d00d9-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="d00d9-130">Chame o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) do novo objeto para salvá-lo.</span><span class="sxs-lookup"><span data-stu-id="d00d9-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="d00d9-131">Atualize a tabela de conteúdo do contêiner para refletir o novo destinatário.</span><span class="sxs-lookup"><span data-stu-id="d00d9-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="d00d9-132">Chamar [IMAPISupport:: Notify](imapisupport-notify.md) para enviar uma notificação de tabela para clientes registrados.</span><span class="sxs-lookup"><span data-stu-id="d00d9-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

