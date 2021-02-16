---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ab21dcfb9011b675e3db4e4df29cb6ecafa6e7c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435345"
---
# <a name="imsgstoregetreceivefolder"></a><span data-ttu-id="18233-103">IMsgStore::GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="18233-103">IMsgStore::GetReceiveFolder</span></span>

  
  
<span data-ttu-id="18233-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18233-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18233-105">Obtém a pasta que foi estabelecida como o destino para mensagens de entrada de uma classe de mensagem especificada ou como a pasta de recebimento padrão para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="18233-105">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a><span data-ttu-id="18233-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18233-106">Parameters</span></span>

 <span data-ttu-id="18233-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="18233-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="18233-108">[in] Um ponteiro para uma classe de mensagem que está associada a uma pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="18233-108">[in] A pointer to a message class that is associated with a receive folder.</span></span> <span data-ttu-id="18233-109">Se o  _parâmetro lpszMessageClass_ for definido como NULL ou uma cadeia de caracteres vazia, **GetReceiveFolder** retornará a pasta de recebimento padrão para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="18233-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **GetReceiveFolder** returns the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="18233-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="18233-110">_ulFlags_</span></span>
  
> <span data-ttu-id="18233-111">[in] Uma máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres passadas e retornadas.</span><span class="sxs-lookup"><span data-stu-id="18233-111">[in] A bitmask of flags that controls the type of the passed-in and returned strings.</span></span> <span data-ttu-id="18233-112">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="18233-112">The following flag can be set:</span></span>
    
<span data-ttu-id="18233-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="18233-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="18233-114">A cadeia de caracteres de classe de mensagem está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="18233-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="18233-115">Se o MAPI_UNICODE sinalizador não estiver definido, a cadeia de caracteres da classe de mensagem está no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="18233-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="18233-116">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="18233-116">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="18233-117">[out] Um ponteiro para a contagem de byte no identificador de entrada apontado pelo _parâmetro lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="18233-117">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="18233-118">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="18233-118">_lppEntryID_</span></span>
  
> <span data-ttu-id="18233-119">[out] Um ponteiro para um ponteiro para o identificador de entrada para a pasta de recebimento solicitada.</span><span class="sxs-lookup"><span data-stu-id="18233-119">[out] A pointer to a pointer to the entry identifier for the requested receive folder.</span></span>
    
 <span data-ttu-id="18233-120">_lppszExplicitClass_</span><span class="sxs-lookup"><span data-stu-id="18233-120">_lppszExplicitClass_</span></span>
  
> <span data-ttu-id="18233-121">[out] Um ponteiro para um ponteiro para a classe de mensagem que define explicitamente como sua pasta de recebimento a pasta apontada por  _lppEntryID_.</span><span class="sxs-lookup"><span data-stu-id="18233-121">[out] A pointer to a pointer to the message class that explicitly sets as its receive folder the folder pointed to by  _lppEntryID_.</span></span> <span data-ttu-id="18233-122">Essa classe de mensagem deve ser a mesma que a classe no parâmetro  _lpszMessageClass_ ou uma classe base dessa classe.</span><span class="sxs-lookup"><span data-stu-id="18233-122">This message class should either be the same as the class in the  _lpszMessageClass_ parameter, or a base class of that class.</span></span> <span data-ttu-id="18233-123">Passar NULL indica que a pasta apontada por  _lppEntryID_ é a pasta de recebimento padrão para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="18233-123">Passing NULL indicates that the folder pointed to by  _lppEntryID_ is the default receive folder for the message store.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="18233-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="18233-124">Return value</span></span>

<span data-ttu-id="18233-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="18233-125">S_OK</span></span> 
  
> <span data-ttu-id="18233-126">A pasta de recebimento foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="18233-126">The receive folder was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18233-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="18233-127">Remarks</span></span>

<span data-ttu-id="18233-128">O **método IMsgStore::GetReceiveFolder** obtém o identificador de entrada de uma pasta de recebimento, uma pasta designada para receber mensagens de entrada de uma classe de mensagem específica.</span><span class="sxs-lookup"><span data-stu-id="18233-128">The **IMsgStore::GetReceiveFolder** method obtains the entry identifier of a receive folder, a folder designated to receive incoming messages of a particular message class.</span></span> <span data-ttu-id="18233-129">Os chamadores podem especificar uma classe de mensagem ou NULL no _parâmetro lpszMessageClass._</span><span class="sxs-lookup"><span data-stu-id="18233-129">Callers can specify a message class or NULL in the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="18233-130">Se  _lpszMessageClass_ for NULL, **GetReceiveFolder** retornará os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="18233-130">If  _lpszMessageClass_ is NULL, **GetReceiveFolder** returns the following values:</span></span> 
  
- <span data-ttu-id="18233-131">Em  _lppszExplicitClass_, o nome da primeira classe base da classe de mensagem apontado por  _lpszMessageClass_ que faz explicitamente definir uma pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="18233-131">In  _lppszExplicitClass_, the name of the first base class of the message class pointed to by  _lpszMessageClass_ that does explicitly set a receive folder.</span></span> 
    
- <span data-ttu-id="18233-132">Em _lppEntryID_, o identificador de entrada da pasta de recebimento para a classe base apontado pelo _parâmetro lppszExplicitClass._</span><span class="sxs-lookup"><span data-stu-id="18233-132">In  _lppEntryID_, the entry identifier of the receive folder for the base class pointed to by the  _lppszExplicitClass_ parameter.</span></span> 
    
<span data-ttu-id="18233-133">Por exemplo, suponha que a pasta de recebimento do IPM da classe de **mensagens. Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM. Note.Phone**.</span><span class="sxs-lookup"><span data-stu-id="18233-133">For example, suppose the receive folder of the message class **IPM.Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM.Note.Phone**.</span></span> <span data-ttu-id="18233-134">Se **IPM. Note.Phone** não tem uma pasta de recebimento explícita definida, **GetReceiveFolder** retorna o identificador de entrada da Caixa de Entrada em  _lppEntryID_ e **IPM. Observação** em  _lppszExplicitClass_.</span><span class="sxs-lookup"><span data-stu-id="18233-134">If **IPM.Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in  _lppEntryID_ and **IPM.Note** in  _lppszExplicitClass_.</span></span>
  
<span data-ttu-id="18233-135">Se o cliente chamar **GetReceiveFolder** para uma classe de mensagem e não tiver definido uma pasta de recebimento para essa classe de mensagem, _lppszExplicitClass_ será uma cadeia de caracteres de comprimento zero, uma cadeia de caracteres no formato Unicode ou uma cadeia de caracteres no formato ANSI, dependendo se o cliente definiu o sinalizador MAPI_UNICODE no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="18233-135">If the client calls **GetReceiveFolder** for a message class and has not set a receive folder for that message class,  _lppszExplicitClass_ is either a zero-length string, a string in Unicode format, or a string in ANSI format depending on whether the client set the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="18233-136">Uma pasta de recebimento padrão, obtida passando NULL no parâmetro  _lpszMessageClass,_ sempre existe para cada armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="18233-136">A default receive folder, obtained by passing NULL in the  _lpszMessageClass_ parameter, always exists for every message store.</span></span> 
  
<span data-ttu-id="18233-137">Um cliente deve chamar a função [MAPIFreeBuffer](mapifreebuffer.md) quando for feito com o identificador de entrada retornado em  _lppEntryID_ para liberar a memória que mantém esse identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="18233-137">A client should call the [MAPIFreeBuffer](mapifreebuffer.md) function when it is done with the entry identifier returned in  _lppEntryID_ to free the memory that holds that entry identifier.</span></span> <span data-ttu-id="18233-138">Ele também deve chamar **MAPIFreeBuffer** quando for feito com a cadeia de caracteres de classe de mensagem retornada em  _lppszExplicitClass_ para liberar a memória que contém essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="18233-138">It should also call **MAPIFreeBuffer** when it is done with the message class string returned in  _lppszExplicitClass_ to free the memory that holds that string.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="18233-139">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="18233-139">MFCMAPI reference</span></span>

<span data-ttu-id="18233-140">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="18233-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="18233-141">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="18233-141">**File**</span></span>|<span data-ttu-id="18233-142">**Função**</span><span class="sxs-lookup"><span data-stu-id="18233-142">**Function**</span></span>|<span data-ttu-id="18233-143">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="18233-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="18233-144">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="18233-144">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="18233-145">GetInbox</span><span class="sxs-lookup"><span data-stu-id="18233-145">GetInbox</span></span>  <br/> |<span data-ttu-id="18233-146">MFCMAPI usa o **método IMsgStore::GetReceiveFolder** para localizar a pasta Caixa de Entrada.</span><span class="sxs-lookup"><span data-stu-id="18233-146">MFCMAPI uses the **IMsgStore::GetReceiveFolder** method to locate the Inbox folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18233-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="18233-147">See also</span></span>



[<span data-ttu-id="18233-148">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="18233-148">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="18233-149">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="18233-149">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="18233-150">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="18233-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

