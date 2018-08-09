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
ms.openlocfilehash: c30c38e1dbc944fd3016badf2621aef5de1e08f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767519"
---
# <a name="imsgstoresetreceivefolder"></a><span data-ttu-id="da623-103">IMsgStore::SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="da623-103">IMsgStore::SetReceiveFolder</span></span>

  
  
<span data-ttu-id="da623-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="da623-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="da623-105">Estabelece uma pasta como destino para mensagens recebidas de uma classe de mensagem específica.</span><span class="sxs-lookup"><span data-stu-id="da623-105">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>
  
```cpp
HRESULT SetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="da623-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da623-106">Parameters</span></span>

 <span data-ttu-id="da623-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="da623-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="da623-108">[in] Um ponteiro para a classe de mensagem que deve ser associado a nova pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="da623-108">[in] A pointer to the message class that is to be associated with the new receive folder.</span></span> <span data-ttu-id="da623-109">Se o parâmetro _lpszMessageClass_ for definido como NULL ou como uma sequência vazia, **SetReceiveFolder** define o padrão receber pasta para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="da623-109">If the  _lpszMessageClass_ parameter is set to NULL or an empty string, **SetReceiveFolder** sets the default receive folder for the message store.</span></span> 
    
 <span data-ttu-id="da623-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="da623-110">_ulFlags_</span></span>
  
> <span data-ttu-id="da623-111">[in] Uma bitmask dos sinalizadores que controla o tipo de texto nas cadeias de caracteres no passado.</span><span class="sxs-lookup"><span data-stu-id="da623-111">[in] A bitmask of flags that controls the type of the text in the passed-in strings.</span></span> <span data-ttu-id="da623-112">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="da623-112">The following flag can be set:</span></span>
    
<span data-ttu-id="da623-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="da623-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="da623-114">A cadeia de caracteres de classe de mensagem está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="da623-114">The message class string is in Unicode format.</span></span> <span data-ttu-id="da623-115">Se o sinalizador MAPI_UNICODE não estiver definido, a cadeia de caracteres de classe de mensagem é no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="da623-115">If the MAPI_UNICODE flag is not set, the message class string is in ANSI format.</span></span>
    
 <span data-ttu-id="da623-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="da623-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="da623-117">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="da623-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="da623-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="da623-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="da623-119">[in] Um ponteiro para o identificador de entrada da pasta para estabelecer como a pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="da623-119">[in] A pointer to the entry identifier of the folder to establish as the receive folder.</span></span> <span data-ttu-id="da623-120">Se o parâmetro _lpEntryID_ for definido como NULL, **SetReceiveFolder** substitui as atuais receber pasta com padrão do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="da623-120">If the  _lpEntryID_ parameter is set to NULL, **SetReceiveFolder** replaces the current receive folder with the message store's default.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="da623-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="da623-121">Return value</span></span>

<span data-ttu-id="da623-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="da623-122">S_OK</span></span> 
  
> <span data-ttu-id="da623-123">Uma pasta de recebimento foi estabelecida com êxito.</span><span class="sxs-lookup"><span data-stu-id="da623-123">A receive folder was successfully established.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="da623-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="da623-124">Remarks</span></span>

<span data-ttu-id="da623-125">O método **IMsgStore::SetReceiveFolder** define ou altera a pasta de recebimento para uma classe de mensagem específica.</span><span class="sxs-lookup"><span data-stu-id="da623-125">The **IMsgStore::SetReceiveFolder** method sets or changes the receive folder for a particular message class.</span></span> <span data-ttu-id="da623-126">Com **SetReceiveFolder**, um cliente pode usando sucessivas chamadas, especificar um diferentes receber a pasta para cada classe de mensagem definidas ou especificar que as mensagens de entrada para várias classes de mensagem todos caminham na mesma pasta.</span><span class="sxs-lookup"><span data-stu-id="da623-126">With **SetReceiveFolder**, a client can, by using successive calls, specify a different receive folder for each defined message class or specify that incoming messages for multiple message classes all go to the same folder.</span></span> <span data-ttu-id="da623-127">Por exemplo, um cliente pode ter sua própria classe de mensagens chegarem na sua própria pasta.</span><span class="sxs-lookup"><span data-stu-id="da623-127">For example, a client can have its own class of messages arrive in its own folder.</span></span> <span data-ttu-id="da623-128">Um aplicativo de fax pode designar uma pasta em que o provedor de armazenamento coloca os faxes de entrada e outra pasta na qual o provedor coloca os faxes de entrada.</span><span class="sxs-lookup"><span data-stu-id="da623-128">A fax application can designate one folder in which the store provider puts incoming faxes and another folder in which the provider puts outgoing faxes.</span></span>
  
<span data-ttu-id="da623-129">Se ocorrer um erro durante a chamada para **SetReceiveFolder**, a configuração da pasta de recebimento permanecerá inalterada.</span><span class="sxs-lookup"><span data-stu-id="da623-129">If an error occurs during the call to **SetReceiveFolder**, the receive folder setting remains unchanged.</span></span> 
  
<span data-ttu-id="da623-130">Se **SetReceiveFolder** altera a configuração da pasta de recebimento com _lpEntryID_ definido como NULL, indicando que a pasta de recebimento padrão deve ser definida, **SetReceiveFolder** Retorna S_OK, mesmo se não havia nenhuma configuração existente para o indicado classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="da623-130">If **SetReceiveFolder** changes the receive folder setting with  _lpEntryID_ set to NULL, indicating that the default receive folder should be set, **SetReceiveFolder** returns S_OK even if there was no existing setting for the indicated message class.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="da623-131">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="da623-131">MFCMAPI reference</span></span>

<span data-ttu-id="da623-132">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="da623-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="da623-133">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="da623-133">**File**</span></span>|<span data-ttu-id="da623-134">**Function**</span><span class="sxs-lookup"><span data-stu-id="da623-134">**Function**</span></span>|<span data-ttu-id="da623-135">**Comment**</span><span class="sxs-lookup"><span data-stu-id="da623-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="da623-136">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="da623-136">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="da623-137">CMsgStoreDlg::OnSetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="da623-137">CMsgStoreDlg::OnSetReceiveFolder</span></span>  <br/> |<span data-ttu-id="da623-138">MFCMAPI usa o método **IMsgStore::SetReceiveFolder** para definir uma pasta como a pasta de recebimento de uma classe de mensagem específica.</span><span class="sxs-lookup"><span data-stu-id="da623-138">MFCMAPI uses the **IMsgStore::SetReceiveFolder** method to set a folder as the receive folder for a particular message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da623-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="da623-139">See also</span></span>



[<span data-ttu-id="da623-140">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="da623-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="da623-141">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="da623-141">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

