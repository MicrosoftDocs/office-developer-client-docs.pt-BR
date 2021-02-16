---
title: OpenTnefStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStream
api_type:
- COM
ms.assetid: 912d7799-53ce-42a7-9fbd-f9a6a3a56047
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 524b52026010b9a06d5822b48b7c04bbf90a113e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423955"
---
# <a name="opentnefstream"></a><span data-ttu-id="3dffd-103">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="3dffd-103">OpenTnefStream</span></span>

<span data-ttu-id="3dffd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3dffd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3dffd-105">Chamado por um provedor de transporte para iniciar uma sessão TNEF (Formato de Encapsulamento Neutro) de Transporte MAPI.</span><span class="sxs-lookup"><span data-stu-id="3dffd-105">Called by a transport provider to initiate a MAPI Transport Neutral Encapsulation Format (TNEF) session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3dffd-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="3dffd-106">Header file:</span></span>  <br/> |<span data-ttu-id="3dffd-107">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="3dffd-107">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="3dffd-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="3dffd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3dffd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3dffd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3dffd-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="3dffd-110">Called by:</span></span>  <br/> |<span data-ttu-id="3dffd-111">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="3dffd-111">Transport providers</span></span>  <br/> |
   
```cpp
HRESULT OpenTnefStream(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName, 
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKey,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a><span data-ttu-id="3dffd-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3dffd-112">Parameters</span></span>

<span data-ttu-id="3dffd-113">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="3dffd-113">_lpvSupport_</span></span>
  
> <span data-ttu-id="3dffd-114">[in] Passa um objeto de suporte ou passa NULL.</span><span class="sxs-lookup"><span data-stu-id="3dffd-114">[in] Passes a support object, or passes in NULL.</span></span> 
    
<span data-ttu-id="3dffd-115">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="3dffd-115">_lpStream_</span></span>
  
> <span data-ttu-id="3dffd-116">[in] Ponteiro para uma interface OLE **IStream** do objeto de fluxo de armazenamento fornecendo uma origem ou destino para uma mensagem de fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="3dffd-116">[in] Pointer to a storage stream object OLE **IStream** interface providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="3dffd-117">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="3dffd-117">_lpszStreamName_</span></span>
  
> <span data-ttu-id="3dffd-118">[in] Ponteiro para o nome do fluxo de dados que o objeto TNEF usa.</span><span class="sxs-lookup"><span data-stu-id="3dffd-118">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="3dffd-119">Se o chamador tiver definido o sinalizador TNEF_ENCODE ( _parâmetro ulFlags)_ em sua chamada para **OpenTnefStream**, o parâmetro  _lpszName_ deverá especificar um ponteiro não nulo para uma cadeia de caracteres não nula consistindo em quaisquer caracteres considerados válidos para nomear um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dffd-119">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="3dffd-120">MAPI does not allow string names including the characters "[", "]" or ":", even if the file system permits their use.</span><span class="sxs-lookup"><span data-stu-id="3dffd-120">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="3dffd-121">O tamanho da cadeia de caracteres passada para  _lpszName_ não deve exceder o valor de MAX_PATH, o comprimento máximo de uma cadeia de caracteres que contém um nome de caminho.</span><span class="sxs-lookup"><span data-stu-id="3dffd-121">The size of the string passed for  _lpszName_ must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="3dffd-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3dffd-122">_ulFlags_</span></span>
  
> <span data-ttu-id="3dffd-123">[in] Bitmask de sinalizadores usados para indicar o modo da função.</span><span class="sxs-lookup"><span data-stu-id="3dffd-123">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="3dffd-124">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="3dffd-124">The following flags can be set:</span></span>
    
<span data-ttu-id="3dffd-125">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="3dffd-125">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="3dffd-126">Todas as propriedades possíveis são mapeadas para seus atributos de nível inferior, mas quando há uma possível perda de dados devido à conversão para um atributo de nível inferior, a propriedade também é codificada nos encapsulamentos.</span><span class="sxs-lookup"><span data-stu-id="3dffd-126">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="3dffd-127">Observe que isso causará a duplicação de informações no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="3dffd-127">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="3dffd-128">TNEF_BEST_DATA padrão se nenhum outro modo for especificado.</span><span class="sxs-lookup"><span data-stu-id="3dffd-128">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="3dffd-129">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="3dffd-129">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="3dffd-130">Fornece compatibilidade com versões mais antigas dos aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="3dffd-130">Provides backward compatibility with the older client applications.</span></span> <span data-ttu-id="3dffd-131">Fluxos TNEF codificados com esse sinalizador mapearão todas as propriedades possíveis para seu atributo de nível inferior correspondente.</span><span class="sxs-lookup"><span data-stu-id="3dffd-131">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="3dffd-132">Esse modo também faz com que o padrão de algumas propriedades que são exigidas por clientes de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="3dffd-132">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="3dffd-133">Esse sinalizador está obsoleto e não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="3dffd-133">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="3dffd-134">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="3dffd-134">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="3dffd-135">O objeto TNEF no fluxo indicado é aberto com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3dffd-135">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="3dffd-136">O provedor de transporte deve definir esse sinalizador se quiser que a função inicialize o objeto para decodificação subsequente.</span><span class="sxs-lookup"><span data-stu-id="3dffd-136">The transport provider must set this flag if it wants the function to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="3dffd-137">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="3dffd-137">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="3dffd-138">O objeto TNEF no fluxo indicado é aberto para permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3dffd-138">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="3dffd-139">O provedor de transporte deve definir esse sinalizador se quiser que a função inicialize o objeto para codificação subsequente.</span><span class="sxs-lookup"><span data-stu-id="3dffd-139">The transport provider must set this flag if it wants the function to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="3dffd-140">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="3dffd-140">TNEF_PURE</span></span> 
  
> <span data-ttu-id="3dffd-141">Codifica todas as propriedades nos blocos de encapsulamento MAPI.</span><span class="sxs-lookup"><span data-stu-id="3dffd-141">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="3dffd-142">Portanto, um arquivo TNEF "puro" consistirá, no máximo, em attMAPIProps, attAttachment, attRenddata e attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="3dffd-142">Therefore, a "pure" TNEF file will consist of, at most, attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="3dffd-143">Esse modo é ideal para uso quando nenhuma compatibilidade com compatibilidade com trás é necessária.</span><span class="sxs-lookup"><span data-stu-id="3dffd-143">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="3dffd-144">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="3dffd-144">_lpMessage_</span></span>
  
> <span data-ttu-id="3dffd-145">[in] Ponteiro para um objeto de mensagem como um destino para uma mensagem decodificada com anexos ou uma fonte para uma mensagem codificada com anexos.</span><span class="sxs-lookup"><span data-stu-id="3dffd-145">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="3dffd-146">Qualquer propriedade de uma mensagem de destino pode ser substituída pelas propriedades de uma mensagem codificada.</span><span class="sxs-lookup"><span data-stu-id="3dffd-146">Any properties of a destination message might be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="3dffd-147">_wKey_</span><span class="sxs-lookup"><span data-stu-id="3dffd-147">_wKey_</span></span>
  
> <span data-ttu-id="3dffd-148">[in] Uma chave de pesquisa que o objeto TNEF usa para corresponder anexos às marcas de texto inseridas no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="3dffd-148">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="3dffd-149">Esse valor deve ser relativamente exclusivo entre mensagens.</span><span class="sxs-lookup"><span data-stu-id="3dffd-149">This value should be relatively unique across messages.</span></span>
    
<span data-ttu-id="3dffd-150">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="3dffd-150">_lppTNEF_</span></span>
  
> <span data-ttu-id="3dffd-151">[out] Ponteiro para o novo objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="3dffd-151">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3dffd-152">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3dffd-152">Return value</span></span>

<span data-ttu-id="3dffd-153">S_OK</span><span class="sxs-lookup"><span data-stu-id="3dffd-153">S_OK</span></span> 
  
> <span data-ttu-id="3dffd-154">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="3dffd-154">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3dffd-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="3dffd-155">Remarks</span></span>

<span data-ttu-id="3dffd-156">Um objeto TNEF criado pela função **OpenTnefStream** chama posteriormente o método OLE **IUnknown::AddRef** para adicionar referências para o objeto de suporte, o objeto de fluxo e o objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3dffd-156">A TNEF object created by the **OpenTnefStream** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="3dffd-157">O provedor de transporte pode liberar as referências para todos os três objetos com uma única chamada para o método **OLE IUnknown::Release** no objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="3dffd-157">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="3dffd-158">**OpenTnefStream** aloca e inicializa uma interface **ITnef** de objeto TNEF para o provedor usar na codificação de uma interface **IMessage** de mensagem MAPI em uma mensagem de fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="3dffd-158">**OpenTnefStream** allocates and initializes a TNEF object **ITnef** interface for the provider to use in encoding a MAPI message **IMessage** interface into a TNEF stream message.</span></span> <span data-ttu-id="3dffd-159">Como alternativa, a função pode configurar o objeto para o provedor usar em chamadas subsequentes para [ITnef::ExtractProps](itnef-extractprops.md) para decodificar uma mensagem de fluxo TNEF em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="3dffd-159">Alternatively, the function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="3dffd-160">Para liberar o objeto TNEF e fechar a sessão, o provedor de transporte deve chamar o método **IUnknown::Release** herdado no objeto.</span><span class="sxs-lookup"><span data-stu-id="3dffd-160">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="3dffd-161">Esta função é o ponto de entrada original para acesso TNEF e foi substituída por [OpenTnefStreamEx,](opentnefstreamex.md) mas ainda é usada para compatibilidade para aqueles que já usam TNEF.</span><span class="sxs-lookup"><span data-stu-id="3dffd-161">This function is the original entry point for TNEF access and has been replaced by [OpenTnefStreamEx](opentnefstreamex.md) but is still used for compatibility for those already using TNEF.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3dffd-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dffd-162">See also</span></span>

- [<span data-ttu-id="3dffd-163">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3dffd-163">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="3dffd-164">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="3dffd-164">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)

