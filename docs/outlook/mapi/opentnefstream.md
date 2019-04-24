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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348920"
---
# <a name="opentnefstream"></a><span data-ttu-id="812a4-103">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="812a4-103">OpenTnefStream</span></span>

<span data-ttu-id="812a4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="812a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="812a4-105">Chamado por um provedor de transporte para iniciar uma sessão do formato de encapsulamento de transporte neutro (TNEF) MAPI.</span><span class="sxs-lookup"><span data-stu-id="812a4-105">Called by a transport provider to initiate a MAPI Transport Neutral Encapsulation Format (TNEF) session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="812a4-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="812a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="812a4-107">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="812a4-107">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="812a4-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="812a4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="812a4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="812a4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="812a4-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="812a4-110">Called by:</span></span>  <br/> |<span data-ttu-id="812a4-111">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="812a4-111">Transport providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="812a4-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="812a4-112">Parameters</span></span>

<span data-ttu-id="812a4-113">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="812a4-113">_lpvSupport_</span></span>
  
> <span data-ttu-id="812a4-114">no Passa um objeto support ou passa NULL.</span><span class="sxs-lookup"><span data-stu-id="812a4-114">[in] Passes a support object, or passes in NULL.</span></span> 
    
<span data-ttu-id="812a4-115">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="812a4-115">_lpStream_</span></span>
  
> <span data-ttu-id="812a4-116">no Ponteiro para um objeto de fluxo de armazenamento interface **IStream** OLE que fornece uma origem ou um destino para uma mensagem de fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="812a4-116">[in] Pointer to a storage stream object OLE **IStream** interface providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="812a4-117">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="812a4-117">_lpszStreamName_</span></span>
  
> <span data-ttu-id="812a4-118">no Ponteiro para o nome do fluxo de dados que o objeto TNEF usa.</span><span class="sxs-lookup"><span data-stu-id="812a4-118">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="812a4-119">Se o chamador tiver definido o sinalizador TNEF_ENCODE (parâmetro _parâmetroulflags_ ) em sua chamada para **OpenTnefStream**, o parâmetro _lpszName_ deverá especificar um ponteiro não nulo para uma cadeia de caracteres não nula que consista em qualquer caractere considerado válido para nomear um arquivo.</span><span class="sxs-lookup"><span data-stu-id="812a4-119">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="812a4-120">O MAPI não permite nomes de cadeia de caracteres, incluindo os caracteres "[", "]" ou ":", mesmo se o sistema de arquivos permitir seu uso.</span><span class="sxs-lookup"><span data-stu-id="812a4-120">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="812a4-121">O tamanho da cadeia de caracteres passada para _lpszName_ não deve exceder o valor de MAX_PATH, o tamanho máximo de uma cadeia de caracteres que contém um nome de caminho.</span><span class="sxs-lookup"><span data-stu-id="812a4-121">The size of the string passed for  _lpszName_ must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="812a4-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="812a4-122">_ulFlags_</span></span>
  
> <span data-ttu-id="812a4-123">no Bitmask dos sinalizadores usados para indicar o modo da função.</span><span class="sxs-lookup"><span data-stu-id="812a4-123">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="812a4-124">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="812a4-124">The following flags can be set:</span></span>
    
<span data-ttu-id="812a4-125">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="812a4-125">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="812a4-126">Todas as propriedades possíveis são mapeadas em seus atributos de nível inferior, mas quando há uma possível perda de dados devido à conversão em um atributo de nível inferior, a propriedade também é codificada nos encapsulamentos.</span><span class="sxs-lookup"><span data-stu-id="812a4-126">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="812a4-127">Observe que isso causará a duplicação de informações no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="812a4-127">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="812a4-128">TNEF_BEST_DATA é o padrão se nenhum outro modo for especificado.</span><span class="sxs-lookup"><span data-stu-id="812a4-128">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="812a4-129">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="812a4-129">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="812a4-130">Fornece compatibilidade com versões anteriores dos aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="812a4-130">Provides backward compatibility with the older client applications.</span></span> <span data-ttu-id="812a4-131">Os fluxos TNEF codificados com esse sinalizador mapearão todas as propriedades possíveis para o atributo de nível inferior correspondente.</span><span class="sxs-lookup"><span data-stu-id="812a4-131">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="812a4-132">Esse modo também faz com que o padrão de algumas propriedades exigidas por clientes de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="812a4-132">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="812a4-133">Este sinalizador é obsoleto e não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="812a4-133">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="812a4-134">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="812a4-134">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="812a4-135">O objeto TNEF no fluxo indicado é aberto com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="812a4-135">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="812a4-136">O provedor de transporte deve definir esse sinalizador se quiser que a função inicialize o objeto para decodificação subsequente.</span><span class="sxs-lookup"><span data-stu-id="812a4-136">The transport provider must set this flag if it wants the function to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="812a4-137">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="812a4-137">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="812a4-138">O objeto TNEF no fluxo indicado é aberto para permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="812a4-138">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="812a4-139">O provedor de transporte deve definir esse sinalizador se quiser que a função inicialize o objeto para a codificação subsequente.</span><span class="sxs-lookup"><span data-stu-id="812a4-139">The transport provider must set this flag if it wants the function to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="812a4-140">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="812a4-140">TNEF_PURE</span></span> 
  
> <span data-ttu-id="812a4-141">Codifica todas as propriedades nos blocos de encapsulamento MAPI.</span><span class="sxs-lookup"><span data-stu-id="812a4-141">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="812a4-142">Portanto, um arquivo TNEF "puro" será composto de, no máximo, attMAPIProps, attAttachment, attRenddata e attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="812a4-142">Therefore, a "pure" TNEF file will consist of, at most, attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="812a4-143">Esse modo é ideal para uso quando não é necessária nenhuma compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="812a4-143">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="812a4-144">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="812a4-144">_lpMessage_</span></span>
  
> <span data-ttu-id="812a4-145">no Ponteiro para um objeto Message como um destino para uma mensagem decodificada com anexos ou uma fonte para uma mensagem codificada com anexos.</span><span class="sxs-lookup"><span data-stu-id="812a4-145">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="812a4-146">Todas as propriedades de uma mensagem de destino podem ser sobrescritas pelas propriedades de uma mensagem codificada.</span><span class="sxs-lookup"><span data-stu-id="812a4-146">Any properties of a destination message might be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="812a4-147">_wKey_</span><span class="sxs-lookup"><span data-stu-id="812a4-147">_wKey_</span></span>
  
> <span data-ttu-id="812a4-148">no Uma chave de pesquisa que o objeto TNEF usa para corresponder anexos às marcas de texto inseridas no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="812a4-148">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="812a4-149">Esse valor deve ser relativamente exclusivo nas mensagens.</span><span class="sxs-lookup"><span data-stu-id="812a4-149">This value should be relatively unique across messages.</span></span>
    
<span data-ttu-id="812a4-150">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="812a4-150">_lppTNEF_</span></span>
  
> <span data-ttu-id="812a4-151">bota Ponteiro para o novo objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="812a4-151">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="812a4-152">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="812a4-152">Return value</span></span>

<span data-ttu-id="812a4-153">S_OK</span><span class="sxs-lookup"><span data-stu-id="812a4-153">S_OK</span></span> 
  
> <span data-ttu-id="812a4-154">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="812a4-154">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="812a4-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="812a4-155">Remarks</span></span>

<span data-ttu-id="812a4-156">Um objeto TNEF criado pela função **OpenTnefStream** , posteriormente, chama o método OLE **IUnknown: AddRef** para adicionar referências para o objeto support, o objeto Stream e o objeto Message.</span><span class="sxs-lookup"><span data-stu-id="812a4-156">A TNEF object created by the **OpenTnefStream** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="812a4-157">O provedor de transporte pode liberar as referências para todos os três objetos com uma única chamada para o método OLE **IUnknown:: Release** no objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="812a4-157">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="812a4-158">**OpenTnefStream** aloca e Inicializa uma interface de objeto **ITnef** do TNEF para o provedor usar na codificação de uma interface de **IMessage** de mensagem MAPI em uma mensagem de fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="812a4-158">**OpenTnefStream** allocates and initializes a TNEF object **ITnef** interface for the provider to use in encoding a MAPI message **IMessage** interface into a TNEF stream message.</span></span> <span data-ttu-id="812a4-159">Como alternativa, a função pode configurar o objeto para o provedor usar em chamadas subsequentes para [ITnef:: ExtractProps](itnef-extractprops.md) para decodificar uma mensagem de fluxo TNEF em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="812a4-159">Alternatively, the function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="812a4-160">Para liberar o objeto TNEF e fechar a sessão, o provedor de transporte deve chamar o método **IUnknown:: Release** herdado no objeto.</span><span class="sxs-lookup"><span data-stu-id="812a4-160">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="812a4-161">Esta função é o ponto de entrada original para acesso TNEF e foi substituído pelo [OpenTnefStreamEx](opentnefstreamex.md) , mas ainda é usado para compatibilidade com aqueles que já usam TNEF.</span><span class="sxs-lookup"><span data-stu-id="812a4-161">This function is the original entry point for TNEF access and has been replaced by [OpenTnefStreamEx](opentnefstreamex.md) but is still used for compatibility for those already using TNEF.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="812a4-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="812a4-162">See also</span></span>

- [<span data-ttu-id="812a4-163">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="812a4-163">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="812a4-164">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="812a4-164">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)

