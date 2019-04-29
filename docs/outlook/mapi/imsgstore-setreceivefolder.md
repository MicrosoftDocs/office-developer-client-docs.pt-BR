---
title: IMsgStoreSetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetReceiveFolder
api_type:
- COM
ms.assetid: 469f0412-1343-47ce-b6e8-e0d5e56c29bb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: efa5d60098fd5f16328669249a8445a124d9878b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434085"
---
# <a name="imsgstoresetreceivefolder"></a><span data-ttu-id="783a5-103">IMsgStore::SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="783a5-103">IMsgStore::SetReceiveFolder</span></span>

  
  
<span data-ttu-id="783a5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="783a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="783a5-105">Estabelece uma pasta como o destino de mensagens de entrada de uma determinada classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="783a5-105">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="783a5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="783a5-106">Parameters</span></span>

 <span data-ttu-id="783a5-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="783a5-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="783a5-108">no Um ponteiro para a classe de mensagem que deve ser associada à nova pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="783a5-108">[in] A pointer to the message class that is to be associated with the new receive folder.</span></span> <span data-ttu-id="783a5-109">Se o parâmetro _lpszMessageClass_ estiver definido como nulo ou uma cadeia de caracteres vazia, **SetReceiveFolder** definirá a pasta de recebimento padrão para o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="783a5-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **SetReceiveFolder** sets the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="783a5-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="783a5-110">_ulFlags_</span></span>
  
> <span data-ttu-id="783a5-111">no Uma máscara de bits de sinalizadores que controla o tipo de texto nas cadeias de caracteres passadas.</span><span class="sxs-lookup"><span data-stu-id="783a5-111">[in] A bitmask of flags that controls the type of the text in the passed-in strings.</span></span> <span data-ttu-id="783a5-112">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="783a5-112">The following flag can be set:</span></span>
    
<span data-ttu-id="783a5-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="783a5-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="783a5-114">A cadeia de caracteres da classe da mensagem está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="783a5-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="783a5-115">Se o sinalizador MAPI_UNICODE não estiver definido, a cadeia de caracteres da classe da mensagem estará no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="783a5-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="783a5-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="783a5-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="783a5-117">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="783a5-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="783a5-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="783a5-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="783a5-119">no Um ponteiro para o identificador de entrada da pasta a ser estabelecida como a pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="783a5-119">[in] A pointer to the entry identifier of the folder to establish as the receive folder.</span></span> <span data-ttu-id="783a5-120">Se o parâmetro _lpEntryID_ estiver definido como nulo, **SetReceiveFolder** substituirá a pasta de recebimento atual pelo padrão do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="783a5-120">If the  _lpEntryID_ parameter is set to NULL, **SetReceiveFolder** replaces the current receive folder with the message store's default.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="783a5-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="783a5-121">Return value</span></span>

<span data-ttu-id="783a5-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="783a5-122">S_OK</span></span> 
  
> <span data-ttu-id="783a5-123">Uma pasta de recebimento foi estabelecida com êxito.</span><span class="sxs-lookup"><span data-stu-id="783a5-123">A receive folder was successfully established.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="783a5-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="783a5-124">Remarks</span></span>

<span data-ttu-id="783a5-125">O método **IMsgStore:: SetReceiveFolder** define ou altera a pasta de recebimento de uma determinada classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="783a5-125">The **IMsgStore::SetReceiveFolder** method sets or changes the receive folder for a particular message class.</span></span> <span data-ttu-id="783a5-126">Com o **SetReceiveFolder**, um cliente pode usar chamadas sucessivas, especificar uma pasta de recebimento diferente para cada classe de mensagem definida ou especificar que as mensagens de entrada para várias classes de mensagens vão para a mesma pasta.</span><span class="sxs-lookup"><span data-stu-id="783a5-126">With **SetReceiveFolder**, a client can, by using successive calls, specify a different receive folder for each defined message class or specify that incoming messages for multiple message classes all go to the same folder.</span></span> <span data-ttu-id="783a5-127">Por exemplo, um cliente pode ter sua própria classe de mensagens chegar em sua própria pasta.</span><span class="sxs-lookup"><span data-stu-id="783a5-127">For example, a client can have its own class of messages arrive in its own folder.</span></span> <span data-ttu-id="783a5-128">Um aplicativo de fax pode designar uma pasta na qual o provedor de repositório coloca faxes de entrada e outra pasta na qual o provedor coloca os faxes de saída.</span><span class="sxs-lookup"><span data-stu-id="783a5-128">A fax application can designate one folder in which the store provider puts incoming faxes and another folder in which the provider puts outgoing faxes.</span></span>
  
<span data-ttu-id="783a5-129">Se ocorrer um erro durante a chamada a **SetReceiveFolder**, a configuração da pasta de recebimento permanecerá inalterada.</span><span class="sxs-lookup"><span data-stu-id="783a5-129">If an error occurs during the call to **SetReceiveFolder**, the receive folder setting remains unchanged.</span></span> 
  
<span data-ttu-id="783a5-130">Se o **SetReceiveFolder** alterar a configuração da pasta de recebimento com _lpEntryID_ definido como nulo, indicando que a pasta de recebimento padrão deve ser definida, **SetReceiveFolder** retornará S_OK, mesmo se não houver nenhuma configuração existente para o indicado classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="783a5-130">If **SetReceiveFolder** changes the receive folder setting with  _lpEntryID_ set to NULL, indicating that the default receive folder should be set, **SetReceiveFolder** returns S_OK even if there was no existing setting for the indicated message class.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="783a5-131">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="783a5-131">MFCMAPI reference</span></span>

<span data-ttu-id="783a5-132">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="783a5-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="783a5-133">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="783a5-133">**File**</span></span>|<span data-ttu-id="783a5-134">**Função**</span><span class="sxs-lookup"><span data-stu-id="783a5-134">**Function**</span></span>|<span data-ttu-id="783a5-135">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="783a5-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="783a5-136">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="783a5-136">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="783a5-137">CMsgStoreDlg:: OnSetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="783a5-137">CMsgStoreDlg::OnSetReceiveFolder</span></span>  <br/> |<span data-ttu-id="783a5-138">MFCMAPI usa o método **IMsgStore:: SetReceiveFolder** para definir uma pasta como a pasta de recebimento para uma determinada classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="783a5-138">MFCMAPI uses the **IMsgStore::SetReceiveFolder** method to set a folder as the receive folder for a particular message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="783a5-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="783a5-139">See also</span></span>



[<span data-ttu-id="783a5-140">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="783a5-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="783a5-141">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="783a5-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

