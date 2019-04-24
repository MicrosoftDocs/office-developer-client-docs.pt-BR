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
ms.openlocfilehash: 4d38648f5e3084c8342fca8d18f0bd3efc915155
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280082"
---
# <a name="imapifoldercreatemessage"></a><span data-ttu-id="c137f-103">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="c137f-103">IMAPIFolder::CreateMessage</span></span>

  
  
<span data-ttu-id="c137f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c137f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c137f-105">Cria uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="c137f-105">Creates a new message.</span></span>
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a><span data-ttu-id="c137f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c137f-106">Parameters</span></span>

 <span data-ttu-id="c137f-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c137f-107">_lpInterface_</span></span>
  
> <span data-ttu-id="c137f-108">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="c137f-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new message.</span></span> <span data-ttu-id="c137f-109">Os identificadores de interface válidos incluem IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer e IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="c137f-109">Valid interface identifiers include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> <span data-ttu-id="c137f-110">Passar NULL faz com que o provedor de repositório de mensagens retorne a interface de mensagens padrão, [IMessage: IMAPIProp](imessageimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="c137f-110">Passing NULL causes the message store provider to return the standard message interface, [IMessage : IMAPIProp](imessageimapiprop.md).</span></span> 
    
 <span data-ttu-id="c137f-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c137f-111">_ulFlags_</span></span>
  
> <span data-ttu-id="c137f-112">no Uma bitmask de sinalizadores que controla como a mensagem é criada.</span><span class="sxs-lookup"><span data-stu-id="c137f-112">[in] A bitmask of flags that controls how the message is created.</span></span> <span data-ttu-id="c137f-113">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="c137f-113">The following flags can be set:</span></span>
    
<span data-ttu-id="c137f-114">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="c137f-114">ITEMPROC_FORCE</span></span>
  
> <span data-ttu-id="c137f-115">Indica o repositório de pastas pessoais (PST) que a mensagem está qualificada para o processamento de regras antes que o repositório Notifique qualquer cliente de escuta da chegada da nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="c137f-115">Indicates to the personal folder store (PST) that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="c137f-116">O processamento de regras só se aplica a novas mensagens criadas em um servidor que não seja do Microsoft Exchange Server, pois o Exchange Server processa as regras para mensagens no servidor.</span><span class="sxs-lookup"><span data-stu-id="c137f-116">Rules processing only applies to new messages that are created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="c137f-117">Portanto, o provedor ou o cliente que cria a mensagem deve passar esse sinalizador em combinação com o salvamento de uma mensagem com [IMAPIPProp:: SaveChanges](imapiprop-savechanges.md) usando NON_EMS_XP_SAVE, que indica que o servidor não é um servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="c137f-117">Therefore, the provider or client creating the message must pass this flag in combination with saving a message with [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) using NON_EMS_XP_SAVE, which indicates that the server is not an Exchange Server.</span></span> 
    
<span data-ttu-id="c137f-118">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="c137f-118">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="c137f-119">A mensagem a ser criada deve ser incluída na tabela de conteúdo associado, em vez da tabela de conteúdo padrão.</span><span class="sxs-lookup"><span data-stu-id="c137f-119">The message to be created should be included in the associated contents table instead of the standard contents table.</span></span> <span data-ttu-id="c137f-120">As mensagens associadas são ocultas da interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c137f-120">Associated messages are hidden from user interaction.</span></span>
    
<span data-ttu-id="c137f-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c137f-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c137f-122">**CreateMessage** tem permissão para ter êxito, mesmo que a operação de criação não tenha sido totalmente concluída.</span><span class="sxs-lookup"><span data-stu-id="c137f-122">**CreateMessage** is allowed to succeed even if the create operation has not fully completed.</span></span> <span data-ttu-id="c137f-123">Isso significa que a nova mensagem pode não estar imediatamente disponível para o chamador.</span><span class="sxs-lookup"><span data-stu-id="c137f-123">This implies that the new message might not be immediately available to the caller.</span></span> 
    
 <span data-ttu-id="c137f-124">_lppMessage_</span><span class="sxs-lookup"><span data-stu-id="c137f-124">_lppMessage_</span></span>
  
> <span data-ttu-id="c137f-125">bota Um ponteiro para um ponteiro para a mensagem recém-criada.</span><span class="sxs-lookup"><span data-stu-id="c137f-125">[out] A pointer to a pointer to the newly created message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c137f-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c137f-126">Return value</span></span>

<span data-ttu-id="c137f-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="c137f-127">S_OK</span></span> 
  
> <span data-ttu-id="c137f-128">A mensagem foi criada com êxito.</span><span class="sxs-lookup"><span data-stu-id="c137f-128">The message was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c137f-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="c137f-129">Remarks</span></span>

<span data-ttu-id="c137f-130">O método **IMAPIFolder:: CreateMessage** cria uma nova mensagem com conteúdo genérico ou associado e atribui um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c137f-130">The **IMAPIFolder::CreateMessage** method creates a new message with generic or associated content and assigns an entry identifier.</span></span> <span data-ttu-id="c137f-131">O identificador de entrada consiste em uma parte que representa o provedor de armazenamento de mensagens e uma parte que representa a mensagem individual.</span><span class="sxs-lookup"><span data-stu-id="c137f-131">The entry identifier consists of a part that represents the message store provider and a part that represents the individual message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c137f-132">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="c137f-132">Notes to implementers</span></span>

<span data-ttu-id="c137f-133">Você pode escolher se deseja definir todas as propriedades de mensagem necessárias em **CreateMessage** ou no método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c137f-133">You can choose whether to set all of the required message properties in **CreateMessage** or in the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="c137f-134">Você não precisa disponibilizar essas propriedades até que uma gravação bem-sucedida tenha ocorrido.</span><span class="sxs-lookup"><span data-stu-id="c137f-134">You do not have to make these properties available until a successful save has occurred.</span></span> 
  
<span data-ttu-id="c137f-135">Para obter mais informações sobre como trabalhar com informações associadas, confira tabelas [de informações associadas a pastas](folder-associated-information-tables.md) e [tabelas de conteúdo](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c137f-135">For more information about how to work with associated information, see [Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables](contents-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c137f-136">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="c137f-136">Notes to callers</span></span>

<span data-ttu-id="c137f-137">Alguns provedores de repositórios de mensagens permitem que o identificador de entrada da nova mensagem fique \*\*\*\* disponível imediatamente após o retorno de CreateMessage; outros provedores de repositórios de mensagens atrasam sua disponibilidade até que a mensagem seja salva.</span><span class="sxs-lookup"><span data-stu-id="c137f-137">Some message store providers allow the entry identifier of the new message to be available immediately after **CreateMessage** returns; other message store providers delay its availability until the message is saved.</span></span> <span data-ttu-id="c137f-138">Como nem todos os provedores de repositório de mensagens geram um identificador de entrada para uma nova mensagem até que você tenha chamado o método **IMAPIProp:: SaveChanges** da mensagem, talvez não seja possível \*\*\*\* acessar o identificador de entrada quando CreateMessage retornar.</span><span class="sxs-lookup"><span data-stu-id="c137f-138">Because not all message store providers generate an entry identifier for a new message until you have called the message's **IMAPIProp::SaveChanges** method, you may be unable to access the entry identifier when **CreateMessage** returns.</span></span> <span data-ttu-id="c137f-139">Além disso, a nova mensagem pode não ser incluída na tabela de conteúdo da pasta até que o salvamento ocorra.</span><span class="sxs-lookup"><span data-stu-id="c137f-139">Also, the new message may not be included in the folder's contents table until the save occurs.</span></span> 
  
<span data-ttu-id="c137f-140">Espere que o identificador de entrada atribuído à nova mensagem seja exclusivo, não apenas no repositório de mensagens atual, mas provavelmente em todos os repositórios de mensagens que estejam abertos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="c137f-140">Expect the entry identifier assigned to the new message to be unique not only in the current message store, but most likely across all of the message stores that are open at the same time.</span></span> <span data-ttu-id="c137f-141">Uma exceção a essa regra ocorre quando várias entradas de um repositório de mensagens aparecem no perfil.</span><span class="sxs-lookup"><span data-stu-id="c137f-141">One exception to this rule occurs when multiple entries for a message store appear in the profile.</span></span> <span data-ttu-id="c137f-142">Isso faz com que o repositório de mensagens seja aberto várias vezes e identificadores de entrada sejam duplicados.</span><span class="sxs-lookup"><span data-stu-id="c137f-142">This causes the message store to be opened multiple times and entry identifiers to be duplicated.</span></span> 
  
<span data-ttu-id="c137f-143">Para criar uma mensagem de saída, chame o método **IMAPIFolder:: CreateMessage** da pasta de saída.</span><span class="sxs-lookup"><span data-stu-id="c137f-143">To create an outgoing message, call the Outbox folder's **IMAPIFolder::CreateMessage** method.</span></span> 
  
<span data-ttu-id="c137f-144">Se você excluir uma pasta que contenha uma nova mensagem antes da mensagem ser salva, os resultados serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="c137f-144">If you delete a folder that contains a new message before the message is saved, the results are undefined.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c137f-145">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c137f-145">MFCMAPI reference</span></span>

<span data-ttu-id="c137f-146">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c137f-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c137f-147">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="c137f-147">**File**</span></span>|<span data-ttu-id="c137f-148">**Função**</span><span class="sxs-lookup"><span data-stu-id="c137f-148">**Function**</span></span>|<span data-ttu-id="c137f-149">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="c137f-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c137f-150">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="c137f-150">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="c137f-151">CFolder:: OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="c137f-151">CFolder::OnNewMessage</span></span>  <br/> |<span data-ttu-id="c137f-152">MFCMAPI usa o método **IMAPIFolder:: CreateMessage** para criar e salvar uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="c137f-152">MFCMAPI uses the **IMAPIFolder::CreateMessage** method to create and save a new message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c137f-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="c137f-153">See also</span></span>



[<span data-ttu-id="c137f-154">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="c137f-154">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="c137f-155">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c137f-155">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="c137f-156">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="c137f-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

