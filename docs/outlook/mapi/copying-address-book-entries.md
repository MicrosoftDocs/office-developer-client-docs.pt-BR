---
title: Copiando entradas do catálogo de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: ce7f7e2db341be62912935b7a55d69eaf5db8ab5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766320"
---
# <a name="copying-address-book-entries"></a><span data-ttu-id="9b655-103">Copiando entradas do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="9b655-103">Copying Address Book Entries</span></span>

  
  
<span data-ttu-id="9b655-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9b655-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9b655-105">Método de [IABContainer::CopyEntries](iabcontainer-copyentries.md) do seu contêiner é chamado quando um ou mais destinatários no mesmo ou outro contêiner devem ser copiados para este contêiner.</span><span class="sxs-lookup"><span data-stu-id="9b655-105">Your container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method is called when one or more recipients from the same or another container are to be copied into this container.</span></span> <span data-ttu-id="9b655-106">**CopyEntries** tem quatro parâmetros de entrada: uma matriz de identificadores de entrada que representa os destinatários a serem copiados, um identificador de janela para o indicador de progresso, um indicador de progresso do objeto e um valor de flags.</span><span class="sxs-lookup"><span data-stu-id="9b655-106">**CopyEntries** has four input parameters: an array of entry identifiers representing the recipients to be copied, a window handle for the progress indicator, a progress object pointer, and a flags value.</span></span> <span data-ttu-id="9b655-107">Seu provedor deve exibir o progresso, se o sinalizador AB_NO_DIALOG não estiver definido e use o objeto de progresso do parâmetro _lpProgress_ se não for nula.</span><span class="sxs-lookup"><span data-stu-id="9b655-107">Your provider should display progress if the AB_NO_DIALOG flag is not set and use the progress object from the  _lpProgress_ parameter if it is not NULL.</span></span> <span data-ttu-id="9b655-108">Se _lpProgress_ for NULL, chame [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) para usar o objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="9b655-108">If  _lpProgress_ is NULL, call [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) to use the MAPI progress object.</span></span> <span data-ttu-id="9b655-109">Para obter mais informações sobre como exibir o progresso, consulte [exibindo um indicador de progresso](mapi-progress-indicators.md).</span><span class="sxs-lookup"><span data-stu-id="9b655-109">For more information about displaying progress, see [Displaying a Progress Indicator](mapi-progress-indicators.md).</span></span>
  
<span data-ttu-id="9b655-110">Além das AB_NO_DIALOG suprimir um indicador de progresso, um dos dois outros sinalizadores pode ser definido como solicitar um tipo de verificação de entrada duplicada: CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT.</span><span class="sxs-lookup"><span data-stu-id="9b655-110">In addition to AB_NO_DIALOG to suppress a progress indicator, one of two other flags can be set to request a type of duplicate entry checking: CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT.</span></span> <span data-ttu-id="9b655-111">Os sinalizadores CREATE_CHECK_DUP_LOOSE e CREATE_CHECK_DUP_STRICT são apenas sugestões sobre como o seu provedor determina entradas duplicadas e podem ser ignorados.</span><span class="sxs-lookup"><span data-stu-id="9b655-111">The CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags are only suggestions as to how your provider determines duplicate entries and can be ignored.</span></span> <span data-ttu-id="9b655-112">MAPI sugere que seu provedor de implementar o suporte para esses sinalizadores da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="9b655-112">MAPI suggests that your provider implement support for these flags as follows.</span></span>
  
|<span data-ttu-id="9b655-113">**Sinalizador de entrada duplicada**</span><span class="sxs-lookup"><span data-stu-id="9b655-113">**Duplicate entry flag**</span></span>|<span data-ttu-id="9b655-114">**Implementação sugerida**</span><span class="sxs-lookup"><span data-stu-id="9b655-114">**Suggested implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b655-115">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="9b655-115">CREATE_CHECK_DUP_LOOSE</span></span>  <br/> |<span data-ttu-id="9b655-116">Verifique se o nome de exibição na entrada a ser criado corresponde ao nome de exibição de uma entrada já no contêiner.</span><span class="sxs-lookup"><span data-stu-id="9b655-116">Check if the display name in the entry to be created matches the display name of an entry already in the container.</span></span>  <br/> |
|<span data-ttu-id="9b655-117">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="9b655-117">CREATE_CHECK_DUP_STRICT</span></span>  <br/> |<span data-ttu-id="9b655-118">Verifique se o nome de exibição e a chave de pesquisa na entrada a ser criado correspondem à chave de nome e a pesquisa de exibição de uma entrada de contêiner.</span><span class="sxs-lookup"><span data-stu-id="9b655-118">Check if both the display name and the search key in the entry to be created match the display name and search key of a container entry.</span></span>  <br/> |
   
<span data-ttu-id="9b655-119">O último sinalizador, CREATE_REPLACE, indica que a nova entrada deve substituir o já existente, se seu provedor determinou que uma entrada a ser criado é uma duplicata de uma entrada já em seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="9b655-119">The last flag, CREATE_REPLACE, indicates that the new entry should replace the existing one if your provider has determined that an entry to be created is a duplicate of an entry already in your container.</span></span> 
  
<span data-ttu-id="9b655-120">Se seu provedor for um catálogo particular de endereços, inclua a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) em cada operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="9b655-120">If your provider is a personal address book, include the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property in every copy operation.</span></span> <span data-ttu-id="9b655-121">Incluindo a tabela de exibição de detalhes de um destinatário copiada permite seu contêiner exibir os detalhes de destinatário em vez de entrar em contato com o contêiner original para criar a exibição.</span><span class="sxs-lookup"><span data-stu-id="9b655-121">Including the details display table of a copied recipient enables your container to display the details of the recipient rather than having to call the original container to create the display.</span></span>
  
 <span data-ttu-id="9b655-122">**Para implementar IABContainer::CopyEntries**</span><span class="sxs-lookup"><span data-stu-id="9b655-122">**To implement IABContainer::CopyEntries**</span></span>
  
1. <span data-ttu-id="9b655-123">Determine se cada identificador de entrada no parâmetro _lpEntries_ está em um formato que seu provedor manipula e se não estiver, falhar e retornar MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="9b655-123">Determine if each entry identifier in the  _lpEntries_ parameter is in a format that your provider handles and if it is not, fail and return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="9b655-124">Se um identificador de entrada representa um usuário de mensagens, lista de distribuição ou contêiner que lida com o seu provedor:</span><span class="sxs-lookup"><span data-stu-id="9b655-124">If an entry identifier represents a messaging user, distribution list, or container that your provider handles:</span></span>
    
1. <span data-ttu-id="9b655-125">Chame o método [IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir o destinatário correspondente.</span><span class="sxs-lookup"><span data-stu-id="9b655-125">Call your [IMAPISupport::OpenEntry](imapisupport-openentry.md) method to open the corresponding recipient.</span></span> 
    
2. <span data-ttu-id="9b655-126">Copie o destinatário para o seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="9b655-126">Copy the recipient to your container.</span></span> 
    
3. <span data-ttu-id="9b655-127">Se o identificador de entrada representa um destinatário externo:</span><span class="sxs-lookup"><span data-stu-id="9b655-127">If the entry identifier represents a foreign recipient:</span></span>
    
1. <span data-ttu-id="9b655-128">Chame o método de [IABContainer::CreateEntry](iabcontainer-createentry.md) do seu contêiner para criar um novo destinatário.</span><span class="sxs-lookup"><span data-stu-id="9b655-128">Call your container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create a new recipient.</span></span> 
    
2. <span data-ttu-id="9b655-129">Definir propriedades iniciais sobre o novo destinatário.</span><span class="sxs-lookup"><span data-stu-id="9b655-129">Set initial properties on the new recipient.</span></span>
    
4. <span data-ttu-id="9b655-130">Chame o novo método do objeto [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para salvá-la.</span><span class="sxs-lookup"><span data-stu-id="9b655-130">Call the new object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it.</span></span> 
    
5. <span data-ttu-id="9b655-131">Atualize a tabela de conteúdo do contêiner para refletir o novo destinatário.</span><span class="sxs-lookup"><span data-stu-id="9b655-131">Update the container's contents table to reflect the new recipient.</span></span> 
    
6. <span data-ttu-id="9b655-132">Chame [IMAPISupport::Notify](imapisupport-notify.md) para enviar uma notificação de tabela para os clientes registrados.</span><span class="sxs-lookup"><span data-stu-id="9b655-132">Call [IMAPISupport::Notify](imapisupport-notify.md) to send a table notification to registered clients.</span></span> 
    

