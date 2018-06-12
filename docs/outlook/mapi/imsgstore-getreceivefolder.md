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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: f58bd8499b63bcd526906f78143b76092f194cb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767488"
---
# <a name="imsgstoregetreceivefolder"></a><span data-ttu-id="b6832-103">IMsgStore::GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="b6832-103">IMsgStore::GetReceiveFolder</span></span>

  
  
<span data-ttu-id="b6832-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6832-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6832-105">Obtém a pasta que foi estabelecida como pasta para o armazenamento de mensagens de recebimento de destino para mensagens recebidas de uma classe de mensagem especificada ou como padrão.</span><span class="sxs-lookup"><span data-stu-id="b6832-105">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a><span data-ttu-id="b6832-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="b6832-106">Parameters</span></span>

 <span data-ttu-id="b6832-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="b6832-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="b6832-108">[in] Um ponteiro para uma classe de mensagem que está associado uma pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="b6832-108">[in] A pointer to a message class that is associated with a receive folder.</span></span> <span data-ttu-id="b6832-109">Se o parâmetro _lpszMessageClass_ for definido como NULL ou como uma sequência vazia, **GetReceiveFolder** retorna o padrão recebem a pasta para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b6832-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **GetReceiveFolder** returns the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="b6832-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b6832-110">_ulFlags_</span></span>
  
> <span data-ttu-id="b6832-111">[in] Uma bitmask dos sinalizadores que controla o tipo das cadeias de caracteres passada-in e retornados.</span><span class="sxs-lookup"><span data-stu-id="b6832-111">[in] A bitmask of flags that controls the type of the passed-in and returned strings.</span></span> <span data-ttu-id="b6832-112">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="b6832-112">The following flag can be set:</span></span>
    
<span data-ttu-id="b6832-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b6832-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b6832-114">A cadeia de caracteres de classe de mensagem está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="b6832-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="b6832-115">Se o sinalizador MAPI_UNICODE não estiver definido, a cadeia de caracteres de classe de mensagem é no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="b6832-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="b6832-116">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b6832-116">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="b6832-117">[out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b6832-117">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b6832-118">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="b6832-118">_lppEntryID_</span></span>
  
> <span data-ttu-id="b6832-119">[out] Pasta de recebimento de um ponteiro para um ponteiro para o identificador de entrada para os solicitados.</span><span class="sxs-lookup"><span data-stu-id="b6832-119">[out] A pointer to a pointer to the entry identifier for the requested receive folder.</span></span>
    
 <span data-ttu-id="b6832-120">_lppszExplicitClass_</span><span class="sxs-lookup"><span data-stu-id="b6832-120">_lppszExplicitClass_</span></span>
  
> <span data-ttu-id="b6832-121">[out] Um ponteiro para um ponteiro para a classe de mensagem que explicitamente define como seu a pasta indicada por _lppEntryID_de pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="b6832-121">[out] A pointer to a pointer to the message class that explicitly sets as its receive folder the folder pointed to by  _lppEntryID_.</span></span> <span data-ttu-id="b6832-122">Esta classe de mensagem deve ser o mesmo que a classe no parâmetro _lpszMessageClass_ , ou uma classe base dessa classe.</span><span class="sxs-lookup"><span data-stu-id="b6832-122">This message class should either be the same as the class in the  _lpszMessageClass_ parameter, or a base class of that class.</span></span> <span data-ttu-id="b6832-123">Passar NULL indica que a pasta indicada por _lppEntryID_ é o padrão receber a pasta para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b6832-123">Passing NULL indicates that the folder pointed to by  _lppEntryID_ is the default receive folder for the message store.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b6832-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b6832-124">Return value</span></span>

<span data-ttu-id="b6832-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6832-125">S_OK</span></span> 
  
> <span data-ttu-id="b6832-126">A pasta de recebimento foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="b6832-126">The receive folder was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b6832-127">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="b6832-127">Remarks</span></span>

<span data-ttu-id="b6832-128">O método **IMsgStore::GetReceiveFolder** obtém o identificador de entrada de uma pasta de recebimento, em uma pasta designada para receber mensagens de entrada de uma classe de mensagem específica.</span><span class="sxs-lookup"><span data-stu-id="b6832-128">The **IMsgStore::GetReceiveFolder** method obtains the entry identifier of a receive folder, a folder designated to receive incoming messages of a particular message class.</span></span> <span data-ttu-id="b6832-129">Os chamadores podem especificar uma classe de mensagem ou NULL no parâmetro _lpszMessageClass_ .</span><span class="sxs-lookup"><span data-stu-id="b6832-129">Callers can specify a message class or NULL in the  _lpszMessageClass_ parameter.</span></span> <span data-ttu-id="b6832-130">Se _lpszMessageClass_ for NULL, **GetReceiveFolder** retorna os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b6832-130">If  _lpszMessageClass_ is NULL, **GetReceiveFolder** returns the following values:</span></span> 
  
- <span data-ttu-id="b6832-131">Em _lppszExplicitClass_, o nome da classe primeira base da classe de mensagem apontado pela _lpszMessageClass_ que definir explicitamente uma pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="b6832-131">In  _lppszExplicitClass_, the name of the first base class of the message class pointed to by  _lpszMessageClass_ that does explicitly set a receive folder.</span></span> 
    
- <span data-ttu-id="b6832-132">Em _lppEntryID_, o identificador de entrada da pasta de recebimento para a classe base apontado pelo parâmetro _lppszExplicitClass_ .</span><span class="sxs-lookup"><span data-stu-id="b6832-132">In  _lppEntryID_, the entry identifier of the receive folder for the base class pointed to by the  _lppszExplicitClass_ parameter.</span></span> 
    
<span data-ttu-id="b6832-133">Por exemplo, suponha que a pasta de recebimento da classe de mensagem **IPM. Observação** tiver sido definida para a entrada identificador da caixa de entrada e **GetReceiveFolder** é chamado com o conteúdo de _lpszMessageClass_ definida como **IPM. Note.Phone**.</span><span class="sxs-lookup"><span data-stu-id="b6832-133">For example, suppose the receive folder of the message class **IPM.Note** has been set to the entry identifier of the Inbox and **GetReceiveFolder** is called with the contents of  _lpszMessageClass_ set to **IPM.Note.Phone**.</span></span> <span data-ttu-id="b6832-134">Se **IPM. Note.Phone** não têm um explícitas recebe conjunto de pastas, **GetReceiveFolder** retorna o identificador de entrada da caixa de entrada no _lppEntryID_ e **IPM. Observação** em _lppszExplicitClass_.</span><span class="sxs-lookup"><span data-stu-id="b6832-134">If **IPM.Note.Phone** does not have an explicit receive folder set, **GetReceiveFolder** returns the entry identifier of the Inbox in  _lppEntryID_ and **IPM.Note** in  _lppszExplicitClass_.</span></span>
  
<span data-ttu-id="b6832-135">Se o cliente chama **GetReceiveFolder** para uma classe de mensagem e não tiver definido uma pasta de recebimento para essa classe de mensagem, _lppszExplicitClass_ é uma cadeia de caracteres de comprimento zero, uma cadeia de caracteres em formato Unicode ou uma cadeia de caracteres, no formato ANSI dependendo se o cliente definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="b6832-135">If the client calls **GetReceiveFolder** for a message class and has not set a receive folder for that message class,  _lppszExplicitClass_ is either a zero-length string, a string in Unicode format, or a string in ANSI format depending on whether the client set the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="b6832-136">Um padrão receber pasta, obtida passando NULL no parâmetro _lpszMessageClass_ , sempre existe para cada armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b6832-136">A default receive folder, obtained by passing NULL in the  _lpszMessageClass_ parameter, always exists for every message store.</span></span> 
  
<span data-ttu-id="b6832-137">Um cliente deve chamar a função [MAPIFreeBuffer](mapifreebuffer.md) quando isso é feito com o identificador de entrada retornado em _lppEntryID_ liberar a memória que contém esse identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="b6832-137">A client should call the [MAPIFreeBuffer](mapifreebuffer.md) function when it is done with the entry identifier returned in  _lppEntryID_ to free the memory that holds that entry identifier.</span></span> <span data-ttu-id="b6832-138">Ele também deve chamar **MAPIFreeBuffer** quando isso é feito com a cadeia de caracteres de classe de mensagem retornada em _lppszExplicitClass_ liberar a memória que contém a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b6832-138">It should also call **MAPIFreeBuffer** when it is done with the message class string returned in  _lppszExplicitClass_ to free the memory that holds that string.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b6832-139">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b6832-139">MFCMAPI reference</span></span>

<span data-ttu-id="b6832-140">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6832-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b6832-141">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b6832-141">**File**</span></span>|<span data-ttu-id="b6832-142">**Function**</span><span class="sxs-lookup"><span data-stu-id="b6832-142">**Function**</span></span>|<span data-ttu-id="b6832-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b6832-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b6832-144">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="b6832-144">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b6832-145">GetInbox</span><span class="sxs-lookup"><span data-stu-id="b6832-145">GetInbox</span></span>  <br/> |<span data-ttu-id="b6832-146">MFCMAPI usa o método **IMsgStore::GetReceiveFolder** para localizar a pasta de caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="b6832-146">MFCMAPI uses the **IMsgStore::GetReceiveFolder** method to locate the Inbox folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6832-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6832-147">See also</span></span>



[<span data-ttu-id="b6832-148">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b6832-148">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b6832-149">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b6832-149">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="b6832-150">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b6832-150">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

