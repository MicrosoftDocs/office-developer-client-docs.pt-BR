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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 154d6e4a4e333f3a6165c3875bdcd57957ebf70c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348731"
---
# <a name="itnefopentaggedbody"></a><span data-ttu-id="e0a19-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="e0a19-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="e0a19-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0a19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0a19-105">Abre uma interface de fluxo no texto de uma mensagem encapsulada.</span><span class="sxs-lookup"><span data-stu-id="e0a19-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="e0a19-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0a19-106">Parameters</span></span>

 <span data-ttu-id="e0a19-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="e0a19-107">_lpMessage_</span></span>
  
> <span data-ttu-id="e0a19-108">[in] Um ponteiro para a mensagem à qual o fluxo está associado.</span><span class="sxs-lookup"><span data-stu-id="e0a19-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="e0a19-109">Essa mensagem não é necessária para ser a mesma mensagem que é passada na chamada para as funções [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="e0a19-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="e0a19-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e0a19-110">_ulFlags_</span></span>
  
> <span data-ttu-id="e0a19-111">[in] Uma máscara de bits de sinalizadores que controla como a interface de fluxo é aberta.</span><span class="sxs-lookup"><span data-stu-id="e0a19-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="e0a19-112">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="e0a19-112">The following flags can be set:</span></span>
    
<span data-ttu-id="e0a19-113">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="e0a19-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="e0a19-114">Se uma propriedade não existir na mensagem atual, ela deverá ser criada.</span><span class="sxs-lookup"><span data-stu-id="e0a19-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="e0a19-115">Se a propriedade existir, os dados atuais na propriedade deverão ser substituídos com os dados do fluxo Transport-Neutral TNEF (Encapsulation Format).</span><span class="sxs-lookup"><span data-stu-id="e0a19-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="e0a19-116">Quando uma implementação define o MAPI_CREATE, ele também deve definir o MAPI_MODIFY sinalizador.</span><span class="sxs-lookup"><span data-stu-id="e0a19-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="e0a19-117">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="e0a19-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="e0a19-118">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e0a19-118">Requests read/write permission.</span></span> <span data-ttu-id="e0a19-119">A interface padrão é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e0a19-119">The default interface is read-only.</span></span> <span data-ttu-id="e0a19-120">MAPI_MODIFY deve ser definido sempre que MAPI_CREATE definida.</span><span class="sxs-lookup"><span data-stu-id="e0a19-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="e0a19-121">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="e0a19-121">_lppStream_</span></span>
  
> <span data-ttu-id="e0a19-122">[out] Um ponteiro para um ponteiro para um objeto de fluxo que contém o texto da propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) da mensagem encapsulada passada e que oferece suporte à interface [IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream)</span><span class="sxs-lookup"><span data-stu-id="e0a19-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e0a19-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e0a19-123">Return value</span></span>

<span data-ttu-id="e0a19-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0a19-124">S_OK</span></span> 
  
> <span data-ttu-id="e0a19-125">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="e0a19-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0a19-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0a19-126">Remarks</span></span>

<span data-ttu-id="e0a19-127">Provedores de transporte, provedores de armazenamento de mensagens e gateways chamam o método **ITnef::OpenTaggedBody** para abrir uma interface de fluxo no texto de uma mensagem encapsulada (ou seja, em um objeto TNEF).</span><span class="sxs-lookup"><span data-stu-id="e0a19-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="e0a19-128">Como parte de seu processamento, **OpenTaggedBody** insere ou analisado marcas de anexo que indicam a posição de quaisquer anexos ou objetos OLE no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e0a19-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="e0a19-129">As marcas de anexo estão no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="e0a19-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="e0a19-130">**[[** _nome do anexo_ **:** n _no_ **nome** _do contêiner do anexo_ **]]**</span><span class="sxs-lookup"><span data-stu-id="e0a19-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="e0a19-131">_o nome do_ anexo descreve o objeto attachment;  _n_ é um número que identifica o anexo que faz parte de uma sequência, incrementando do valor passado no parâmetro  _lpKey_ da função [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx;](opentnefstreamex.md) e  _o nome do contêiner_ de anexo descreve o componente físico em que o objeto anexo reside.</span><span class="sxs-lookup"><span data-stu-id="e0a19-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="e0a19-132">**OpenTaggedBody** lê o texto da mensagem e insere uma marca de anexo sempre que um objeto de anexo apareceu originalmente no texto.</span><span class="sxs-lookup"><span data-stu-id="e0a19-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="e0a19-133">O texto da mensagem original não é alterado.</span><span class="sxs-lookup"><span data-stu-id="e0a19-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="e0a19-134">Quando uma mensagem com marcas é passada para um fluxo, as marcas são retiradas e os objetos de anexo são realocados na posição das marcas no fluxo.</span><span class="sxs-lookup"><span data-stu-id="e0a19-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e0a19-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0a19-135">See also</span></span>



[<span data-ttu-id="e0a19-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="e0a19-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="e0a19-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="e0a19-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="e0a19-138">Propriedade canônica PidTagBody</span><span class="sxs-lookup"><span data-stu-id="e0a19-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="e0a19-139">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0a19-139">ITnef : IUnknown</span></span>](itnefiunknown.md)

