---
title: Copiar ou mover uma mensagem ou uma pasta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Modificado pela última vez: 08 de novembro de 2011'
ms.openlocfilehash: 97e7c90c2fdc715d7d0749300cc62854fffa6447
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563979"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a><span data-ttu-id="4be3f-103">Copiar ou mover uma mensagem ou uma pasta</span><span class="sxs-lookup"><span data-stu-id="4be3f-103">Copying or moving a message or a folder</span></span>
  
<span data-ttu-id="4be3f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4be3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4be3f-105">Um cliente pode usar um dos quatro métodos para copiar ou mover uma mensagem ou uma pasta:</span><span class="sxs-lookup"><span data-stu-id="4be3f-105">A client can use one of four methods to copy or move a message or a folder:</span></span>
  
- [<span data-ttu-id="4be3f-106">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="4be3f-106">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
- [<span data-ttu-id="4be3f-107">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="4be3f-107">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
- [<span data-ttu-id="4be3f-108">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="4be3f-108">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="4be3f-109">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="4be3f-109">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
<span data-ttu-id="4be3f-110">Definindo os parâmetros e os sinalizadores apropriados, **CopyTo** e **CopyProps** podem ser feitas para funcionar como **CopyFolder** ou **CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="4be3f-110">By setting the appropriate flags and parameters, **CopyTo** and **CopyProps** can be made to work just like **CopyFolder** or **CopyMessages**.</span></span> <span data-ttu-id="4be3f-111">Ao decidir qual método de chamada, considere as seguintes questões:</span><span class="sxs-lookup"><span data-stu-id="4be3f-111">Consider the following issues when deciding which method to call:</span></span>
  
- <span data-ttu-id="4be3f-112">Você copiar ou mover uma pasta ou uma mensagem?</span><span class="sxs-lookup"><span data-stu-id="4be3f-112">Are you copying or moving a folder or a message?</span></span>
    
- <span data-ttu-id="4be3f-113">Quanto você sabe sobre a pasta ou a mensagem a ser movido ou copiadas?</span><span class="sxs-lookup"><span data-stu-id="4be3f-113">How much do you know about the folder or message to be moved or copied?</span></span>
    
- <span data-ttu-id="4be3f-114">Quantos da pasta ou propriedades da mensagem serão movidas ou copiadas?</span><span class="sxs-lookup"><span data-stu-id="4be3f-114">How many of the folder or message's properties will be moved or copied?</span></span>
    
<span data-ttu-id="4be3f-115">Você pode usar os métodos **IMAPIProp** para copiar ou mover uma pasta ou uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="4be3f-115">You can use the **IMAPIProp** methods to copy or move either a folder or a message.</span></span> <span data-ttu-id="4be3f-116">**IMAPIFolder::CopyMessages** funciona com mensagens apenas; **IMAPIFolder::CopyFolder** funciona com pastas apenas.</span><span class="sxs-lookup"><span data-stu-id="4be3f-116">**IMAPIFolder::CopyMessages** works with messages only; **IMAPIFolder::CopyFolder** works with folders only.</span></span> 
  
<span data-ttu-id="4be3f-117">Enquanto usando os métodos **IMAPIFolder** não requer nenhum conhecimento das propriedades compatíveis com a pasta ou mensagem devem ser copiados ou movidos, você deve ter algum conhecimento usar os métodos **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="4be3f-117">Whereas using the **IMAPIFolder** methods does not require any knowledge of the properties supported by the folder or message to be copied or moved, you must have some knowledge to use the **IMAPIProp** methods.</span></span> <span data-ttu-id="4be3f-118">Com **IMAPIProp::CopyProps**, você deve ser capaz de especificar explicitamente que as propriedades de pasta ou uma mensagem que você deseja copiar ou mover.</span><span class="sxs-lookup"><span data-stu-id="4be3f-118">With **IMAPIProp::CopyProps**, you must be able to explicitly specify which of the folder or message properties that you want to copy or move.</span></span> <span data-ttu-id="4be3f-119">Com **IMAPIProp::CopyTo**, a menos que você deseja copiar ou mover todas as propriedades, você deve especificar explicitamente quais devem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="4be3f-119">With **IMAPIProp::CopyTo**, unless you want to copy or move all of the properties, you must explicitly specify which ones should be excluded.</span></span> <span data-ttu-id="4be3f-120">Para obter mais informações sobre esses métodos, consulte [Copiando propriedades de MAPI](copying-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="4be3f-120">For more information about these methods, see [Copying MAPI Properties](copying-mapi-properties.md).</span></span>
  
<span data-ttu-id="4be3f-121">O número de propriedades devem ser copiados ou movidos pode afetar sua decisão sobre qual método usar.</span><span class="sxs-lookup"><span data-stu-id="4be3f-121">The number of properties to be copied or moved can affect your decision as to which method to use.</span></span> <span data-ttu-id="4be3f-122">Se você estiver copiar ou mover várias mensagens, chame **IMAPIFolder::CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="4be3f-122">If you are copying or moving multiple messages, call **IMAPIFolder::CopyMessages**.</span></span> <span data-ttu-id="4be3f-123">Escolha uma alternativa é chamar **IMAPIProp::CopyProps** para copiar somente as propriedades da pasta **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4be3f-123">An alternate choice is to call **IMAPIProp::CopyProps** to copy only the folder's **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span> <span data-ttu-id="4be3f-124">O procedimento a seguir mostra como usar **CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="4be3f-124">The following procedure shows how to use **CopyMessages**.</span></span> 
  
### <a name="to-copy-or-move-one-or-more-messages"></a><span data-ttu-id="4be3f-125">Para copiar ou mover uma ou mais mensagens</span><span class="sxs-lookup"><span data-stu-id="4be3f-125">To copy or move one or more messages</span></span>
  
1. <span data-ttu-id="4be3f-126">Localize os identificadores de entrada válida para as pastas de origem e destino.</span><span class="sxs-lookup"><span data-stu-id="4be3f-126">Locate valid entry identifiers for the source and destination folders.</span></span>
    
2. <span data-ttu-id="4be3f-127">Abra essas pastas no modo leitura/gravação chamando [IMAPISession::OpenEntry](imapisession-openentry.md) ou [IMsgStore::OpenEntry](imsgstore-openentry.md) e definindo o sinalizador MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="4be3f-127">Open these folders in read/write mode by calling either [IMAPISession::OpenEntry](imapisession-openentry.md) or [IMsgStore::OpenEntry](imsgstore-openentry.md) and setting the MAPI_MODIFY flag.</span></span> 
    
3. <span data-ttu-id="4be3f-128">Verifique se o ponteiro de interface retornado da **OpenEntry** é um ponteiro de interface **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="4be3f-128">Check that the interface pointer returned from **OpenEntry** is an **IMAPIFolder** interface pointer.</span></span> <span data-ttu-id="4be3f-129">Caso contrário, converta-a para o tipo LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="4be3f-129">If not, cast it to the LPMAPIFOLDER type.</span></span> 
    
4. <span data-ttu-id="4be3f-130">Crie uma matriz de identificadores de entrada que representa uma ou mais mensagens devem ser copiados ou movidos.</span><span class="sxs-lookup"><span data-stu-id="4be3f-130">Create an array of entry identifiers representing the one or more messages to be copied or moved.</span></span> 
    
5. <span data-ttu-id="4be3f-131">Chame **IMAPIFolder::CopyMessages** com o conjunto de sinalizadores a seguir:</span><span class="sxs-lookup"><span data-stu-id="4be3f-131">Call **IMAPIFolder::CopyMessages** with the following flags set:</span></span> 
    
   - <span data-ttu-id="4be3f-132">MESSAGE_MOVE, se você quiser realizar uma operação de movimentação.</span><span class="sxs-lookup"><span data-stu-id="4be3f-132">MESSAGE_MOVE, if you want to perform a move operation.</span></span> 
    
   - <span data-ttu-id="4be3f-133">MESSAGE_DIALOG e passar uma janela manipulam no parâmetro _ulUIParam_ , se quiser que a pasta para mostrar um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="4be3f-133">MESSAGE_DIALOG and pass a window handle in the  _ulUIParam_ parameter, if you want the folder to show a progress indicator.</span></span> 
    
6. <span data-ttu-id="4be3f-134">Libere os ponteiros **IMAPIFolder** para as pastas de origem e destino.</span><span class="sxs-lookup"><span data-stu-id="4be3f-134">Release the **IMAPIFolder** pointers for the source and destination folders.</span></span> 
    
<span data-ttu-id="4be3f-135">Se você desejar copiar todo o conteúdo de uma pasta para outra pasta, chame o método de **IMAPIFolder::CopyFolder** ou **IMAPIProp::CopyTo** da pasta de origem.</span><span class="sxs-lookup"><span data-stu-id="4be3f-135">If you want to copy the complete contents of a folder to another folder, call the source folder's **IMAPIFolder::CopyFolder** or **IMAPIProp::CopyTo** method.</span></span> 
  
<span data-ttu-id="4be3f-136">Para copiar algumas das propriedades de uma pasta, chame seu método de **IMAPIProp::CopyProps** .</span><span class="sxs-lookup"><span data-stu-id="4be3f-136">To copy a few of a folder's properties, call its **IMAPIProp::CopyProps** method.</span></span> <span data-ttu-id="4be3f-137">Para copiar a maioria das propriedades de uma pasta, chame **IMAPIProp::CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="4be3f-137">To copy most of a folder's properties, call **IMAPIProp::CopyTo**.</span></span> 
  
<span data-ttu-id="4be3f-138">Por exemplo, se desejar copiar **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e propriedades de **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) de uma pasta, você tem as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="4be3f-138">For example, if you want to copy a folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) properties, you have the following options:</span></span>
  
- <span data-ttu-id="4be3f-139">Chame **IMAPIFolder::CopyFolder** para copiar todas as propriedades de pasta e exclua aqueles indesejadas da nova pasta.</span><span class="sxs-lookup"><span data-stu-id="4be3f-139">Call **IMAPIFolder::CopyFolder** to copy all of the folder properties and then delete the unwanted ones from the new folder.</span></span> 
    
- <span data-ttu-id="4be3f-140">Chame **CopyTo** e exclua todas as propriedades da pasta exceto **PR_DISPLAY_NAME** e **PR_COMMENT**.</span><span class="sxs-lookup"><span data-stu-id="4be3f-140">Call **CopyTo** and exclude all of the folder's properties except for **PR_DISPLAY_NAME** and **PR_COMMENT**.</span></span> 
    
- <span data-ttu-id="4be3f-141">Chame **CopyProps**, passando a matriz de incluir **PR_DISPLAY_NAME** e **PR_COMMENT** .</span><span class="sxs-lookup"><span data-stu-id="4be3f-141">Call **CopyProps**, passing **PR_DISPLAY_NAME** and **PR_COMMENT** in the include array.</span></span> 
    
<span data-ttu-id="4be3f-142">Nesse caso, **CopyProps** é a melhor opção, pois ele se destina a ser usado para copiar um pequeno conjunto de propriedades e é a chamada mais fácil para implementar.</span><span class="sxs-lookup"><span data-stu-id="4be3f-142">In this case, **CopyProps** is the best choice because it is meant to be used to copy a small set of properties and is the easiest call to implement.</span></span> 
  
<span data-ttu-id="4be3f-143">Para copiar ou mover somente as propriedades de pasta, sem incluir mensagens, chame o método de **IMAPIProp::CopyTo** da pasta e excluir as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="4be3f-143">To copy or move only folder properties, without including messages, call the folder's **IMAPIProp::CopyTo** method and exclude the following properties:</span></span> 
  
- <span data-ttu-id="4be3f-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4be3f-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>
    
- <span data-ttu-id="4be3f-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4be3f-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>
    
<span data-ttu-id="4be3f-146">Os métodos de cópia podem retornar S_OK, indicando sucesso total, MAPI_W_PARTIAL_COMPLETION, indicando êxito parcial, ou um erro.</span><span class="sxs-lookup"><span data-stu-id="4be3f-146">The copy methods can return S_OK, indicating total success, MAPI_W_PARTIAL_COMPLETION, indicating partial success, or an error.</span></span> <span data-ttu-id="4be3f-147">Se MAPI_W_PARTIAL_COMPLETION for retornada, use a macro **HR_FAILED** para acessar um erro mais específico.</span><span class="sxs-lookup"><span data-stu-id="4be3f-147">If MAPI_W_PARTIAL_COMPLETION is returned, use the **HR_FAILED** macro to access a more specific error.</span></span> <span data-ttu-id="4be3f-148">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="4be3f-148">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
  
<span data-ttu-id="4be3f-149">Se você copiar mensagens do repositório de uma mensagem para outro e Unicode não é suportado para ambos, lembre-se de que as informações podem ser perdidas devido à conversão de página de código.</span><span class="sxs-lookup"><span data-stu-id="4be3f-149">If you copy messages from one message store to another and Unicode is not supported by both, be aware that information can be lost due to code page conversion.</span></span> <span data-ttu-id="4be3f-150">Geralmente você não pode saber se os repositórios de mensagem dão suporte a formatos de um ou ambos, tornando impossível determinar se deseja copiar as propriedades de texto, como sequências de caracteres ASCII ou como sequências de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="4be3f-150">Usually you cannot know if the message stores support one or both formats, making it impossible to determine whether to copy text properties as ASCII strings or as Unicode strings.</span></span> <span data-ttu-id="4be3f-151">Caso você ofereça suporte a Unicode, tente realizar uma cópia de Unicode; Se ele falhar com o valor de erro MAPI_E_BAD_CHARWIDTH, recorrer a ASCII.</span><span class="sxs-lookup"><span data-stu-id="4be3f-151">If you support Unicode, try to perform a Unicode copy; if it fails with the error value MAPI_E_BAD_CHARWIDTH, resort to ASCII.</span></span>
  

