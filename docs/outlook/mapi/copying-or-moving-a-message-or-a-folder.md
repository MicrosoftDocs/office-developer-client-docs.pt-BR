---
title: Copiar ou mover uma mensagem ou uma pasta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Última modificação: 08 de novembro de 2011'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333037"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a><span data-ttu-id="97f78-103">Copiar ou mover uma mensagem ou uma pasta</span><span class="sxs-lookup"><span data-stu-id="97f78-103">Copying or moving a message or a folder</span></span>
  
<span data-ttu-id="97f78-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97f78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97f78-105">Um cliente pode usar um dos quatro métodos para copiar ou mover uma mensagem ou uma pasta:</span><span class="sxs-lookup"><span data-stu-id="97f78-105">A client can use one of four methods to copy or move a message or a folder:</span></span>
  
- [<span data-ttu-id="97f78-106">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="97f78-106">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
- [<span data-ttu-id="97f78-107">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="97f78-107">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
- [<span data-ttu-id="97f78-108">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="97f78-108">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="97f78-109">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="97f78-109">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
<span data-ttu-id="97f78-110">Configurando os sinalizadores e parâmetros apropriados, **CopyTo** e **CopyProps** podem ser feitos para funcionar da mesma forma que o **CopyFolder** ou o **CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="97f78-110">By setting the appropriate flags and parameters, **CopyTo** and **CopyProps** can be made to work just like **CopyFolder** or **CopyMessages**.</span></span> <span data-ttu-id="97f78-111">Considere os seguintes problemas ao decidir qual método chamar:</span><span class="sxs-lookup"><span data-stu-id="97f78-111">Consider the following issues when deciding which method to call:</span></span>
  
- <span data-ttu-id="97f78-112">Você está copiando ou movendo uma pasta ou uma mensagem?</span><span class="sxs-lookup"><span data-stu-id="97f78-112">Are you copying or moving a folder or a message?</span></span>
    
- <span data-ttu-id="97f78-113">Quanto você sabe sobre a pasta ou a mensagem a ser movida ou copiada?</span><span class="sxs-lookup"><span data-stu-id="97f78-113">How much do you know about the folder or message to be moved or copied?</span></span>
    
- <span data-ttu-id="97f78-114">Quantas Propriedades da pasta ou da mensagem serão movidas ou copiadas?</span><span class="sxs-lookup"><span data-stu-id="97f78-114">How many of the folder or message's properties will be moved or copied?</span></span>
    
<span data-ttu-id="97f78-115">Você pode usar os métodos **IMAPIProp** para copiar ou mover uma pasta ou uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="97f78-115">You can use the **IMAPIProp** methods to copy or move either a folder or a message.</span></span> <span data-ttu-id="97f78-116">**IMAPIFolder:: CopyMessages** funciona somente com mensagens; **IMAPIFolder:: CopyFolder** funciona somente com pastas.</span><span class="sxs-lookup"><span data-stu-id="97f78-116">**IMAPIFolder::CopyMessages** works with messages only; **IMAPIFolder::CopyFolder** works with folders only.</span></span> 
  
<span data-ttu-id="97f78-117">Enquanto o uso dos métodos **IMAPIFolder** não exige nenhum conhecimento das propriedades com suporte na pasta ou na mensagem a ser copiada ou movida, você deve ter algum conhecimento para usar os métodos **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="97f78-117">Whereas using the **IMAPIFolder** methods does not require any knowledge of the properties supported by the folder or message to be copied or moved, you must have some knowledge to use the **IMAPIProp** methods.</span></span> <span data-ttu-id="97f78-118">Com o **IMAPIProp:: CopyProps**, você deve ser capaz de especificar explicitamente quais das propriedades de pasta ou de mensagem que você deseja copiar ou mover.</span><span class="sxs-lookup"><span data-stu-id="97f78-118">With **IMAPIProp::CopyProps**, you must be able to explicitly specify which of the folder or message properties that you want to copy or move.</span></span> <span data-ttu-id="97f78-119">Com **IMAPIProp:: CopyTo**, a menos que você queira copiar ou mover todas as propriedades, você deve especificar explicitamente quais delas devem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="97f78-119">With **IMAPIProp::CopyTo**, unless you want to copy or move all of the properties, you must explicitly specify which ones should be excluded.</span></span> <span data-ttu-id="97f78-120">Para obter mais informações sobre esses métodos, consulte [copyING MAPI Properties](copying-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="97f78-120">For more information about these methods, see [Copying MAPI Properties](copying-mapi-properties.md).</span></span>
  
<span data-ttu-id="97f78-121">O número de propriedades a serem copiadas ou movidas pode afetar sua decisão quanto ao método a ser usado.</span><span class="sxs-lookup"><span data-stu-id="97f78-121">The number of properties to be copied or moved can affect your decision as to which method to use.</span></span> <span data-ttu-id="97f78-122">Se você estiver copiando ou movendo várias mensagens, chame **IMAPIFolder:: CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="97f78-122">If you are copying or moving multiple messages, call **IMAPIFolder::CopyMessages**.</span></span> <span data-ttu-id="97f78-123">Uma opção alternativa é chamar **IMAPIProp:: CopyProps** para copiar apenas a propriedade **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) da pasta.</span><span class="sxs-lookup"><span data-stu-id="97f78-123">An alternate choice is to call **IMAPIProp::CopyProps** to copy only the folder's **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span> <span data-ttu-id="97f78-124">O procedimento a seguir mostra como usar o **CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="97f78-124">The following procedure shows how to use **CopyMessages**.</span></span> 
  
### <a name="to-copy-or-move-one-or-more-messages"></a><span data-ttu-id="97f78-125">Para copiar ou mover uma ou mais mensagens</span><span class="sxs-lookup"><span data-stu-id="97f78-125">To copy or move one or more messages</span></span>
  
1. <span data-ttu-id="97f78-126">Localize identificadores de entrada válidos para as pastas de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="97f78-126">Locate valid entry identifiers for the source and destination folders.</span></span>
    
2. <span data-ttu-id="97f78-127">Abra essas pastas no modo de leitura/gravação chamando [IMAPISession:: OpenEntry](imapisession-openentry.md) ou [IMsgStore:: OpenEntry](imsgstore-openentry.md) e definindo o sinalizador MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="97f78-127">Open these folders in read/write mode by calling either [IMAPISession::OpenEntry](imapisession-openentry.md) or [IMsgStore::OpenEntry](imsgstore-openentry.md) and setting the MAPI_MODIFY flag.</span></span> 
    
3. <span data-ttu-id="97f78-128">Verifique se o ponteiro de interface retornado de **OpenEntry** é um ponteiro de interface **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="97f78-128">Check that the interface pointer returned from **OpenEntry** is an **IMAPIFolder** interface pointer.</span></span> <span data-ttu-id="97f78-129">Caso contrário, converta-o para o tipo LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="97f78-129">If not, cast it to the LPMAPIFOLDER type.</span></span> 
    
4. <span data-ttu-id="97f78-130">Criar uma matriz de identificadores de entrada que representam uma ou mais mensagens a serem copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="97f78-130">Create an array of entry identifiers representing the one or more messages to be copied or moved.</span></span> 
    
5. <span data-ttu-id="97f78-131">Chamar **IMAPIFolder:: CopyMessages** com os seguintes sinalizadores definidos:</span><span class="sxs-lookup"><span data-stu-id="97f78-131">Call **IMAPIFolder::CopyMessages** with the following flags set:</span></span> 
    
   - <span data-ttu-id="97f78-132">MESSAGE_MOVE, se você quiser realizar uma operação de movimentação.</span><span class="sxs-lookup"><span data-stu-id="97f78-132">MESSAGE_MOVE, if you want to perform a move operation.</span></span> 
    
   - <span data-ttu-id="97f78-133">MESSAGE_DIALOG e passe um identificador de janela no parâmetro _ulUIParam_ , se você quiser que a pasta mostre um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="97f78-133">MESSAGE_DIALOG and pass a window handle in the  _ulUIParam_ parameter, if you want the folder to show a progress indicator.</span></span> 
    
6. <span data-ttu-id="97f78-134">Libere os ponteiros do **IMAPIFolder** para as pastas de origem e destino.</span><span class="sxs-lookup"><span data-stu-id="97f78-134">Release the **IMAPIFolder** pointers for the source and destination folders.</span></span> 
    
<span data-ttu-id="97f78-135">Se você quiser copiar todo o conteúdo de uma pasta para outra pasta, chame o método **IMAPIFolder:: CopyFolder** ou **IMAPIProp:** : a pasta de origem.</span><span class="sxs-lookup"><span data-stu-id="97f78-135">If you want to copy the complete contents of a folder to another folder, call the source folder's **IMAPIFolder::CopyFolder** or **IMAPIProp::CopyTo** method.</span></span> 
  
<span data-ttu-id="97f78-136">Para copiar algumas das propriedades de uma pasta, chame seu método **IMAPIProp:: CopyProps** .</span><span class="sxs-lookup"><span data-stu-id="97f78-136">To copy a few of a folder's properties, call its **IMAPIProp::CopyProps** method.</span></span> <span data-ttu-id="97f78-137">Para copiar a maioria das propriedades de uma pasta, chame **IMAPIProp:: CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="97f78-137">To copy most of a folder's properties, call **IMAPIProp::CopyTo**.</span></span> 
  
<span data-ttu-id="97f78-138">Por exemplo, se você deseja copiar as propriedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) de uma pasta, você tem as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="97f78-138">For example, if you want to copy a folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) properties, you have the following options:</span></span>
  
- <span data-ttu-id="97f78-139">Chame **IMAPIFolder:: CopyFolder** para copiar todas as propriedades da pasta e exclua os indesejados da nova pasta.</span><span class="sxs-lookup"><span data-stu-id="97f78-139">Call **IMAPIFolder::CopyFolder** to copy all of the folder properties and then delete the unwanted ones from the new folder.</span></span> 
    
- <span data-ttu-id="97f78-140">Chame **CopyTo** e exclua todas as propriedades da pasta, exceto **PR_DISPLAY_NAME** e **PR_COMMENT**.</span><span class="sxs-lookup"><span data-stu-id="97f78-140">Call **CopyTo** and exclude all of the folder's properties except for **PR_DISPLAY_NAME** and **PR_COMMENT**.</span></span> 
    
- <span data-ttu-id="97f78-141">Chame **CopyProps**, passando **PR_DISPLAY_NAME** e **PR_COMMENT** na matriz include.</span><span class="sxs-lookup"><span data-stu-id="97f78-141">Call **CopyProps**, passing **PR_DISPLAY_NAME** and **PR_COMMENT** in the include array.</span></span> 
    
<span data-ttu-id="97f78-142">Nesse caso, **CopyProps** é a melhor opção porque deve ser usada para copiar um pequeno conjunto de propriedades e é a chamada mais fácil de implementar.</span><span class="sxs-lookup"><span data-stu-id="97f78-142">In this case, **CopyProps** is the best choice because it is meant to be used to copy a small set of properties and is the easiest call to implement.</span></span> 
  
<span data-ttu-id="97f78-143">Para copiar ou mover somente as propriedades da pasta, sem incluir as mensagens, chame o método **IMAPIProp:: CopyTo** da pasta e exclua as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="97f78-143">To copy or move only folder properties, without including messages, call the folder's **IMAPIProp::CopyTo** method and exclude the following properties:</span></span> 
  
- <span data-ttu-id="97f78-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="97f78-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>
    
- <span data-ttu-id="97f78-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="97f78-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>
    
<span data-ttu-id="97f78-146">Os métodos Copy podem retornar S_OK, indicando o êxito total, MAPI_W_PARTIAL_COMPLETION, indicando o êxito parcial ou um erro.</span><span class="sxs-lookup"><span data-stu-id="97f78-146">The copy methods can return S_OK, indicating total success, MAPI_W_PARTIAL_COMPLETION, indicating partial success, or an error.</span></span> <span data-ttu-id="97f78-147">Se MAPI_W_PARTIAL_COMPLETION for retornado, use a macro **HR_FAILED** para acessar um erro mais específico.</span><span class="sxs-lookup"><span data-stu-id="97f78-147">If MAPI_W_PARTIAL_COMPLETION is returned, use the **HR_FAILED** macro to access a more specific error.</span></span> <span data-ttu-id="97f78-148">Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="97f78-148">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
  
<span data-ttu-id="97f78-149">Se você copiar mensagens de um repositório de mensagens para outro e Unicode não for suportada por ambas, lembre-se de que as informações podem ser perdidas devido à conversão da página de código.</span><span class="sxs-lookup"><span data-stu-id="97f78-149">If you copy messages from one message store to another and Unicode is not supported by both, be aware that information can be lost due to code page conversion.</span></span> <span data-ttu-id="97f78-150">Normalmente, você não pode saber se os repositórios de mensagens dão suporte a um ou ambos formatos, tornando impossível determinar se as propriedades de texto serão copiadas como cadeias de caracteres ASCII ou como cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="97f78-150">Usually you cannot know if the message stores support one or both formats, making it impossible to determine whether to copy text properties as ASCII strings or as Unicode strings.</span></span> <span data-ttu-id="97f78-151">Se você oferecer suporte a Unicode, tente executar uma cópia Unicode; Se ele falhar com o valor de erro MAPI_E_BAD_CHARWIDTH, recorrer a ASCII.</span><span class="sxs-lookup"><span data-stu-id="97f78-151">If you support Unicode, try to perform a Unicode copy; if it fails with the error value MAPI_E_BAD_CHARWIDTH, resort to ASCII.</span></span>
  

