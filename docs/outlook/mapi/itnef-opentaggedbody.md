---
title: ITnefOpenTaggedBody
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.OpenTaggedBody
api_type:
- COM
ms.assetid: 70d5b34c-85b3-4d1f-860e-2838947ba428
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 14964f367e3dbca484c4e1612b374a6a72ddf17b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593778"
---
# <a name="itnefopentaggedbody"></a><span data-ttu-id="f3215-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="f3215-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="f3215-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3215-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3215-105">Abre uma interface de fluxo no texto de uma mensagem encapsulado.</span><span class="sxs-lookup"><span data-stu-id="f3215-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="f3215-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3215-106">Parameters</span></span>

 <span data-ttu-id="f3215-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="f3215-107">_lpMessage_</span></span>
  
> <span data-ttu-id="f3215-108">[in] Um ponteiro para a mensagem com a qual o stream está associado.</span><span class="sxs-lookup"><span data-stu-id="f3215-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="f3215-109">Esta mensagem não é necessária para ser a mesma mensagem que é passada na chamada para a função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="f3215-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="f3215-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f3215-110">_ulFlags_</span></span>
  
> <span data-ttu-id="f3215-111">[in] Uma bitmask dos sinalizadores que controla como a interface do fluxo é aberta.</span><span class="sxs-lookup"><span data-stu-id="f3215-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="f3215-112">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="f3215-112">The following flags can be set:</span></span>
    
<span data-ttu-id="f3215-113">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="f3215-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="f3215-114">Se uma propriedade não existir na mensagem atual, ele deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="f3215-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="f3215-115">Se a propriedade existir, os dados atuais na propriedade devem ser substituídos com os dados do fluxo de Transport-Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="f3215-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="f3215-116">Quando uma implementação define o sinalizador MAPI_CREATE, ele também deve definir o sinalizador MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="f3215-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="f3215-117">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="f3215-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="f3215-118">Permissão de leitura/gravação solicitações.</span><span class="sxs-lookup"><span data-stu-id="f3215-118">Requests read/write permission.</span></span> <span data-ttu-id="f3215-119">A interface padrão é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f3215-119">The default interface is read-only.</span></span> <span data-ttu-id="f3215-120">MAPI_MODIFY deve ser definida sempre que MAPI_CREATE é definida.</span><span class="sxs-lookup"><span data-stu-id="f3215-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="f3215-121">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="f3215-121">_lppStream_</span></span>
  
> <span data-ttu-id="f3215-122">[out] Um ponteiro para um ponteiro para um objeto stream que contém o texto da propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) de passados-in encapsulado mensagem e que dá suporte à interface [IStream](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="f3215-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f3215-123">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f3215-123">Return value</span></span>

<span data-ttu-id="f3215-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3215-124">S_OK</span></span> 
  
> <span data-ttu-id="f3215-125">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="f3215-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3215-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3215-126">Remarks</span></span>

<span data-ttu-id="f3215-127">Provedores de transporte, provedores de armazenamento de mensagem e gateways chame o método de **ITnef::OpenTaggedBody** para abrir uma interface de fluxo no texto de uma mensagem encapsulado (ou seja, um TNEF do objeto).</span><span class="sxs-lookup"><span data-stu-id="f3215-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="f3215-128">Como parte do seu processamento, **OpenTaggedBody** insere ou analisa as marcas de anexo que indicam a posição de todos os anexos ou objetos OLE no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f3215-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="f3215-129">As marcas de anexo são no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="f3215-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="f3215-130">**[[** o _nome do anexo_ **:** _n_ **no** _nome do contêiner de anexo_ **]]**</span><span class="sxs-lookup"><span data-stu-id="f3215-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="f3215-131">_nome do anexo_ descreve o objeto de anexo;  _n_ é um número que identifica o anexo que faz parte de uma sequência, incrementar do valor passado no parâmetro _lpKey_ do [OpenTnefStream](opentnefstream.md) ou função [OpenTnefStreamEx](opentnefstreamex.md) ; e _o nome de contêiner de anexo_ descreve o componente físico onde o objeto de anexo reside.</span><span class="sxs-lookup"><span data-stu-id="f3215-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="f3215-132">**OpenTaggedBody** lê o texto de mensagem e insere uma marca de anexo sempre que um objeto attachment aparecia originalmente no texto.</span><span class="sxs-lookup"><span data-stu-id="f3215-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="f3215-133">O texto da mensagem original não é alterado.</span><span class="sxs-lookup"><span data-stu-id="f3215-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="f3215-134">Quando uma mensagem que tenha marcas é passada para um stream, as marcas serão perdidas e os objetos attachment contidos forem realocados na posição das marcas no stream.</span><span class="sxs-lookup"><span data-stu-id="f3215-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f3215-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3215-135">See also</span></span>



[<span data-ttu-id="f3215-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="f3215-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="f3215-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="f3215-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="f3215-138">Propriedade canônica PidTagBody</span><span class="sxs-lookup"><span data-stu-id="f3215-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="f3215-139">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f3215-139">ITnef : IUnknown</span></span>](itnefiunknown.md)

