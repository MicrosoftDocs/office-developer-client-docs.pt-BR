---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e740e86fc25307457119aabf6e2aa0c42a9d69b9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568221"
---
# <a name="imapifoldercreatemessage"></a><span data-ttu-id="bb4b3-103">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="bb4b3-103">IMAPIFolder::CreateMessage</span></span>

  
  
<span data-ttu-id="bb4b3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb4b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb4b3-105">Cria uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-105">Creates a new message.</span></span>
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a><span data-ttu-id="bb4b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb4b3-106">Parameters</span></span>

 <span data-ttu-id="bb4b3-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="bb4b3-107">_lpInterface_</span></span>
  
> <span data-ttu-id="bb4b3-108">[in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new message.</span></span> <span data-ttu-id="bb4b3-109">Identificadores de interface válidos incluem IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer e IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-109">Valid interface identifiers include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> <span data-ttu-id="bb4b3-110">Passar NULL faz com que o provedor de armazenamento de mensagem retornar a interface de mensagem padrão, [IMessage: IMAPIProp](imessageimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="bb4b3-110">Passing NULL causes the message store provider to return the standard message interface, [IMessage : IMAPIProp](imessageimapiprop.md).</span></span> 
    
 <span data-ttu-id="bb4b3-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bb4b3-111">_ulFlags_</span></span>
  
> <span data-ttu-id="bb4b3-112">[in] Uma bitmask dos sinalizadores que controla como a mensagem é criada.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-112">[in] A bitmask of flags that controls how the message is created.</span></span> <span data-ttu-id="bb4b3-113">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="bb4b3-113">The following flags can be set:</span></span>
    
<span data-ttu-id="bb4b3-114">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="bb4b3-114">ITEMPROC_FORCE</span></span>
  
> <span data-ttu-id="bb4b3-115">Indica para o repositório de pasta particular (. PST) que a mensagem é qualificada para regras de processamento antes que o repositório notificará qualquer cliente escuta a partir da chegada da nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-115">Indicates to the personal folder store (PST) that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="bb4b3-116">Processamento apenas das regras se aplica às novas mensagens que são criadas em um servidor que não seja um Microsoft Exchange Server, pois o Exchange Server processa as regras para mensagens no servidor.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-116">Rules processing only applies to new messages that are created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="bb4b3-117">Portanto, o provedor ou criar a mensagem de cliente deve passar por esse sinalizador em combinação com o salvamento de uma mensagem com [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) usando NON_EMS_XP_SAVE, que indica que o servidor não é um servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-117">Therefore, the provider or client creating the message must pass this flag in combination with saving a message with [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) using NON_EMS_XP_SAVE, which indicates that the server is not an Exchange Server.</span></span> 
    
<span data-ttu-id="bb4b3-118">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="bb4b3-118">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="bb4b3-119">A mensagem a ser criado deve ser incluída na tabela de conteúdo associado no lugar do índice de conteúdo padrão.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-119">The message to be created should be included in the associated contents table instead of the standard contents table.</span></span> <span data-ttu-id="bb4b3-120">Mensagens associadas estão ocultos na interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-120">Associated messages are hidden from user interaction.</span></span>
    
<span data-ttu-id="bb4b3-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="bb4b3-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="bb4b3-122">**CreateMessage** é permitido tenha êxito, mesmo se a operação de criação não foi totalmente concluída.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-122">**CreateMessage** is allowed to succeed even if the create operation has not fully completed.</span></span> <span data-ttu-id="bb4b3-123">Isso significa que a nova mensagem pode não estar disponível imediatamente ao chamador.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-123">This implies that the new message might not be immediately available to the caller.</span></span> 
    
 <span data-ttu-id="bb4b3-124">_lppMessage_</span><span class="sxs-lookup"><span data-stu-id="bb4b3-124">_lppMessage_</span></span>
  
> <span data-ttu-id="bb4b3-125">[out] Um ponteiro para um ponteiro para a mensagem recém-criado.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-125">[out] A pointer to a pointer to the newly created message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bb4b3-126">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bb4b3-126">Return value</span></span>

<span data-ttu-id="bb4b3-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb4b3-127">S_OK</span></span> 
  
> <span data-ttu-id="bb4b3-128">A mensagem foi criada com êxito.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-128">The message was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bb4b3-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb4b3-129">Remarks</span></span>

<span data-ttu-id="bb4b3-130">O método **IMAPIFolder::CreateMessage** cria uma nova mensagem com conteúdo genérico ou associado e atribui um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-130">The **IMAPIFolder::CreateMessage** method creates a new message with generic or associated content and assigns an entry identifier.</span></span> <span data-ttu-id="bb4b3-131">O identificador de entrada consiste em uma parte que representa o provedor de armazenamento de mensagem e uma parte que representa a mensagem individual.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-131">The entry identifier consists of a part that represents the message store provider and a part that represents the individual message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bb4b3-132">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="bb4b3-132">Notes to implementers</span></span>

<span data-ttu-id="bb4b3-133">Você pode escolher se deseja definir todas as propriedades de mensagem necessária no **CreateMessage** ou no método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-133">You can choose whether to set all of the required message properties in **CreateMessage** or in the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="bb4b3-134">Você não precisará disponibilizar essas propriedades até que uma gravação bem-sucedida tenha ocorrido.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-134">You do not have to make these properties available until a successful save has occurred.</span></span> 
  
<span data-ttu-id="bb4b3-135">Para obter mais informações sobre como trabalhar com informações associadas, consulte [Folder-Associated tabelas de informações](folder-associated-information-tables.md) e [Conteúdo](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="bb4b3-135">For more information about how to work with associated information, see [Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables](contents-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bb4b3-136">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="bb4b3-136">Notes to callers</span></span>

<span data-ttu-id="bb4b3-137">Alguns provedores de repositório de mensagem permitem o identificador de entrada da nova mensagem estejam disponíveis imediatamente após **CreateMessage** retorna; outros provedores de armazenamento de mensagem atrasam a sua disponibilidade até que a mensagem será salva.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-137">Some message store providers allow the entry identifier of the new message to be available immediately after **CreateMessage** returns; other message store providers delay its availability until the message is saved.</span></span> <span data-ttu-id="bb4b3-138">Porque nem todos os provedores de armazenamento de mensagem geram um identificador de entrada para uma nova mensagem, até que você tenha chamado o método de **IMAPIProp::SaveChanges** da mensagem, você pode ser capaz de acessar o identificador de entrada quando **CreateMessage** retorna.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-138">Because not all message store providers generate an entry identifier for a new message until you have called the message's **IMAPIProp::SaveChanges** method, you may be unable to access the entry identifier when **CreateMessage** returns.</span></span> <span data-ttu-id="bb4b3-139">Além disso, a nova mensagem pode não ser incluída na tabela de conteúdo da pasta até que ocorra a salvar.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-139">Also, the new message may not be included in the folder's contents table until the save occurs.</span></span> 
  
<span data-ttu-id="bb4b3-140">Espere o identificador de entrada atribuído à nova mensagem ser exclusivas não apenas no armazenamento da mensagem atual, mas bem provável em todos os repositórios de mensagem que estão abertos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-140">Expect the entry identifier assigned to the new message to be unique not only in the current message store, but most likely across all of the message stores that are open at the same time.</span></span> <span data-ttu-id="bb4b3-141">Uma exceção a essa regra ocorre quando várias entradas para um armazenamento de mensagens aparecem no perfil.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-141">One exception to this rule occurs when multiple entries for a message store appear in the profile.</span></span> <span data-ttu-id="bb4b3-142">Isso faz com que o armazenamento de mensagens a serem abertas várias vezes e os identificadores de entrada a ser duplicado.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-142">This causes the message store to be opened multiple times and entry identifiers to be duplicated.</span></span> 
  
<span data-ttu-id="bb4b3-143">Para criar uma mensagem de saída, chame o método de **IMAPIFolder::CreateMessage** da pasta caixa de saída.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-143">To create an outgoing message, call the Outbox folder's **IMAPIFolder::CreateMessage** method.</span></span> 
  
<span data-ttu-id="bb4b3-144">Se você excluir uma pasta que contém uma nova mensagem antes que a mensagem será salva, os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-144">If you delete a folder that contains a new message before the message is saved, the results are undefined.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bb4b3-145">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bb4b3-145">MFCMAPI reference</span></span>

<span data-ttu-id="bb4b3-146">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bb4b3-147">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="bb4b3-147">**File**</span></span>|<span data-ttu-id="bb4b3-148">**Function**</span><span class="sxs-lookup"><span data-stu-id="bb4b3-148">**Function**</span></span>|<span data-ttu-id="bb4b3-149">**Comment**</span><span class="sxs-lookup"><span data-stu-id="bb4b3-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bb4b3-150">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="bb4b3-150">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="bb4b3-151">CFolder::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="bb4b3-151">CFolder::OnNewMessage</span></span>  <br/> |<span data-ttu-id="bb4b3-152">MFCMAPI usa o método **IMAPIFolder::CreateMessage** para criar e salvar uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb4b3-152">MFCMAPI uses the **IMAPIFolder::CreateMessage** method to create and save a new message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb4b3-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb4b3-153">See also</span></span>



[<span data-ttu-id="bb4b3-154">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="bb4b3-154">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="bb4b3-155">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="bb4b3-155">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="bb4b3-156">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="bb4b3-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

