---
title: OpenTnefStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStreamEx
api_type:
- COM
ms.assetid: eb84c408-2d8b-453b-92f4-5fd8851b84ca
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b651a913855e99e2f26dfd99fb725cc332201932
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565183"
---
# <a name="opentnefstreamex"></a><span data-ttu-id="57b5a-103">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="57b5a-103">OpenTnefStreamEx</span></span>

<span data-ttu-id="57b5a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57b5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57b5a-105">Cria um objeto Transport-Neutral Encapsulation Format (TNEF) que pode ser usado para codificar ou decodificar um objeto de mensagem em um fluxo de dados TNEF para uso por transportes ou gateways e repositórios de mensagem.</span><span class="sxs-lookup"><span data-stu-id="57b5a-105">Creates a Transport-Neutral Encapsulation Format (TNEF) object that can be used to encode or decode a message object into a TNEF data stream for use by transports or gateways and message stores.</span></span> <span data-ttu-id="57b5a-106">Este é o ponto de entrada para acesso TNEF.</span><span class="sxs-lookup"><span data-stu-id="57b5a-106">This is the entry point for TNEF access.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57b5a-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="57b5a-107">Header file:</span></span>  <br/> |<span data-ttu-id="57b5a-108">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="57b5a-108">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="57b5a-109">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="57b5a-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="57b5a-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="57b5a-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="57b5a-111">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="57b5a-111">Called by:</span></span>  <br/> |<span data-ttu-id="57b5a-112">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="57b5a-112">Transport providers</span></span>  <br/> |
   
```cpp
HRESULT OpenTnefStreamEx(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName,
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKeyVal,
  LPADDRESSBOOK lpAddressBook,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a><span data-ttu-id="57b5a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57b5a-113">Parameters</span></span>

<span data-ttu-id="57b5a-114">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="57b5a-114">_lpvSupport_</span></span>
  
> <span data-ttu-id="57b5a-115">[in] Passa um objeto de suporte ou passa em nulo.</span><span class="sxs-lookup"><span data-stu-id="57b5a-115">[in] Passes a support object, or passes in NULL.</span></span> <span data-ttu-id="57b5a-116">Se for NULL, o parâmetro _lpAddressBook_ deve ser não-nulos.</span><span class="sxs-lookup"><span data-stu-id="57b5a-116">If NULL, the  _lpAddressBook_ parameter should be non-null.</span></span> 
    
<span data-ttu-id="57b5a-117">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="57b5a-117">_lpStream_</span></span>
  
> <span data-ttu-id="57b5a-118">[in] Ponteiro para um objeto stream de armazenamento, como uma interface **IStream** do OLE, fornecendo origem ou destino para uma mensagem de fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="57b5a-118">[in] Pointer to a storage stream object, such as an OLE **IStream** interface, providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="57b5a-119">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="57b5a-119">_lpszStreamName_</span></span>
  
> <span data-ttu-id="57b5a-120">[in] Ponteiro para o nome do fluxo de dados que usa o objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="57b5a-120">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="57b5a-121">Se o chamador tiver configurado o sinalizador TNEF_ENCODE (parâmetro _ulFlags_ ) na sua chamada **OpenTnefStream**, o parâmetro _lpszName_ deve especificar um ponteiro de não-nulo para uma cadeia de caracteres não-nulos consistindo quaisquer caracteres considerados válidos para nomear um arquivo.</span><span class="sxs-lookup"><span data-stu-id="57b5a-121">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="57b5a-122">MAPI não permite nomes de cadeia de caracteres, incluindo os caracteres "[", "]", ou ":", mesmo se o seu uso permite que o sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="57b5a-122">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="57b5a-123">O tamanho da cadeia de caracteres passada para o parâmetro _lpszName_ não deve exceder o valor da MAX_PATH, o comprimento máximo de uma cadeia de caracteres que contém um nome de caminho.</span><span class="sxs-lookup"><span data-stu-id="57b5a-123">The size of the string passed for the  _lpszName_ parameter must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="57b5a-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="57b5a-124">_ulFlags_</span></span>
  
> <span data-ttu-id="57b5a-125">[in] Bitmask dos sinalizadores usados para indicar o modo da função.</span><span class="sxs-lookup"><span data-stu-id="57b5a-125">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="57b5a-126">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="57b5a-126">The following flags can be set:</span></span>
    
<span data-ttu-id="57b5a-127">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="57b5a-127">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="57b5a-128">Todas as propriedades possíveis são mapeadas em seus atributos de baixo nível, mas, quando há uma possível perda de dados devido à conversão para um atributo de baixo nível, a propriedade também é codificada nos encapsulamentos.</span><span class="sxs-lookup"><span data-stu-id="57b5a-128">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="57b5a-129">Observe que isso fará com que a duplicação de informações no stream TNEF.</span><span class="sxs-lookup"><span data-stu-id="57b5a-129">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="57b5a-130">TNEF_BEST_DATA é o padrão se nenhum outros meios forem especificados.</span><span class="sxs-lookup"><span data-stu-id="57b5a-130">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="57b5a-131">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="57b5a-131">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="57b5a-132">Fornece a compatibilidade com versões anteriores com aplicativos mais antigos do cliente.</span><span class="sxs-lookup"><span data-stu-id="57b5a-132">Provides backward compatibility with older client applications.</span></span> <span data-ttu-id="57b5a-133">Fluxos TNEF codificados com esse sinalizador mapeará todas as propriedades possíveis em seu atributo de baixo nível correspondente.</span><span class="sxs-lookup"><span data-stu-id="57b5a-133">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="57b5a-134">Este modo também fará com que o padrão é de algumas propriedades que são exigidas por clientes de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="57b5a-134">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="57b5a-135">Esse sinalizador é obsoleto e não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="57b5a-135">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="57b5a-136">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="57b5a-136">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="57b5a-137">O objeto TNEF no fluxo indicado é aberto com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="57b5a-137">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="57b5a-138">O provedor de transporte deve definir esse sinalizador se a função for inicializar o objeto de decodificação subsequentes.</span><span class="sxs-lookup"><span data-stu-id="57b5a-138">The transport provider must set this flag if the function is to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="57b5a-139">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="57b5a-139">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="57b5a-140">O objeto TNEF no fluxo indicado é aberto para permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="57b5a-140">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="57b5a-141">O provedor de transporte deve definir esse sinalizador se a função for inicializar o objeto para a codificação subsequentes.</span><span class="sxs-lookup"><span data-stu-id="57b5a-141">The transport provider must set this flag if the function is to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="57b5a-142">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="57b5a-142">TNEF_PURE</span></span> 
  
> <span data-ttu-id="57b5a-143">Codifica todas as propriedades nos blocos de encapsulamento de MAPI.</span><span class="sxs-lookup"><span data-stu-id="57b5a-143">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="57b5a-144">Portanto, um arquivo TNEF "puro" consistirá em, no máximo, os atributos attMAPIProps, attAttachment, attRenddata e attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="57b5a-144">Therefore, a "pure" TNEF file will consist of, at most, the attributes attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="57b5a-145">Esse modo é ideal para uso quando sem compatibilidade com versões anteriores é necessária.</span><span class="sxs-lookup"><span data-stu-id="57b5a-145">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="57b5a-146">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="57b5a-146">_lpMessage_</span></span>
  
> <span data-ttu-id="57b5a-147">[in] Ponteiro para um objeto de mensagem como um destino para uma mensagem decodificada com anexos ou em uma fonte de mensagem codificada com anexos.</span><span class="sxs-lookup"><span data-stu-id="57b5a-147">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="57b5a-148">Todas as propriedades de uma mensagem de destino podem ser substituídas pelas propriedades de uma mensagem codificada.</span><span class="sxs-lookup"><span data-stu-id="57b5a-148">Any properties of a destination message can be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="57b5a-149">_wKeyVal_</span><span class="sxs-lookup"><span data-stu-id="57b5a-149">_wKeyVal_</span></span>
  
> <span data-ttu-id="57b5a-150">[in] Uma chave de pesquisa que o objeto TNEF usa para corresponder os anexos para as marcas de texto inseridos no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="57b5a-150">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="57b5a-151">Este valor deve ser exclusivo relativamente nas mensagens.</span><span class="sxs-lookup"><span data-stu-id="57b5a-151">This value should be relatively unique across messages.</span></span> 
    
<span data-ttu-id="57b5a-152">_lpAddressBook_</span><span class="sxs-lookup"><span data-stu-id="57b5a-152">_lpAddressBook_</span></span>
  
> <span data-ttu-id="57b5a-153">[in] Ponteiro para um objeto de catálogo de endereços usado para obter as informações de identificadores de entrada de endereçamento.</span><span class="sxs-lookup"><span data-stu-id="57b5a-153">[in] Pointer to an address book object used to get addressing information for entry identifiers.</span></span> 
    
<span data-ttu-id="57b5a-154">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="57b5a-154">_lppTNEF_</span></span>
  
> <span data-ttu-id="57b5a-155">[out] Ponteiro para o novo objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="57b5a-155">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="57b5a-156">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="57b5a-156">Return value</span></span>

<span data-ttu-id="57b5a-157">S_OK</span><span class="sxs-lookup"><span data-stu-id="57b5a-157">S_OK</span></span> 
  
> <span data-ttu-id="57b5a-158">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="57b5a-158">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57b5a-159">Comentários</span><span class="sxs-lookup"><span data-stu-id="57b5a-159">Remarks</span></span>

<span data-ttu-id="57b5a-160">A função **OpenTnefStreamEx** é o substituto recomendado para [OpenTnefStream](opentnefstream.md), o ponto de entrada original para acesso TNEF.</span><span class="sxs-lookup"><span data-stu-id="57b5a-160">The **OpenTnefStreamEx** function is the recommended replacement for [OpenTnefStream](opentnefstream.md), the original entry point for TNEF access.</span></span> 
  
<span data-ttu-id="57b5a-161">Um objeto TNEF criado pela função **OpenTnefStreamEx** posteriormente chama o método OLE **AddRef** adicionar referências para o objeto de suporte, o objeto stream e o objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="57b5a-161">A TNEF object created by the **OpenTnefStreamEx** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="57b5a-162">O provedor de transporte pode liberar as referências para todos os três objetos com uma única chamada ao método OLE **IUnknown:: Release** no objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="57b5a-162">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="57b5a-163">**OpenTnefStreamEx** aloca e inicializa um objeto TNEF para o provedor a ser usado em uma mensagem MAPI de codificação em uma mensagem de fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="57b5a-163">**OpenTnefStreamEx** allocates and initializes a TNEF object for the provider to use in encoding a MAPI message into a TNEF stream message.</span></span> <span data-ttu-id="57b5a-164">Como alternativa, essa função pode configurar o objeto para o provedor a ser usado em chamadas subsequentes para [ITnef::ExtractProps](itnef-extractprops.md) para decodificar uma mensagem de fluxo TNEF em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="57b5a-164">Alternatively, this function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="57b5a-165">Para liberar o objeto TNEF e fechar a sessão, o provedor de transporte deve chamar o método **IUnknown:: Release** herdado no objeto.</span><span class="sxs-lookup"><span data-stu-id="57b5a-165">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="57b5a-166">O valor de base para o parâmetro _wKeyVal_ não deve ser zero e não deve ser o mesmo para cada chamada para **OpenTnefStreamEx**.</span><span class="sxs-lookup"><span data-stu-id="57b5a-166">The base value for the  _wKeyVal_ parameter must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="57b5a-167">Em vez disso, use números aleatórios com base na hora do sistema do gerador de números aleatórios da biblioteca de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="57b5a-167">Instead, use random numbers based on the system time from the run-time library's random number generator.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="57b5a-168">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="57b5a-168">MFCMAPI reference</span></span>

<span data-ttu-id="57b5a-169">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="57b5a-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="57b5a-170">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="57b5a-170">**File**</span></span>|<span data-ttu-id="57b5a-171">**Function**</span><span class="sxs-lookup"><span data-stu-id="57b5a-171">**Function**</span></span>|<span data-ttu-id="57b5a-172">**Comment**</span><span class="sxs-lookup"><span data-stu-id="57b5a-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="57b5a-173">CPP</span><span class="sxs-lookup"><span data-stu-id="57b5a-173">File.cpp</span></span>  <br/> |<span data-ttu-id="57b5a-174">LoadFromTNEF</span><span class="sxs-lookup"><span data-stu-id="57b5a-174">LoadFromTNEF</span></span>  <br/> |<span data-ttu-id="57b5a-175">MFCMAPI usa o método **OpenTnefStreamEx** para abrir um fluxo no arquivo TNEF, portanto, podem ser extraídas propriedades.</span><span class="sxs-lookup"><span data-stu-id="57b5a-175">MFCMAPI uses the **OpenTnefStreamEx** method to open a stream on the TNEF file so properties may be extracted.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57b5a-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="57b5a-176">See also</span></span>

- [<span data-ttu-id="57b5a-177">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="57b5a-177">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="57b5a-178">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="57b5a-178">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="57b5a-179">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="57b5a-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

