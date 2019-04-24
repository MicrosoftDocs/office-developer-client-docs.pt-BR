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
ms.openlocfilehash: 178ab67875d8fb442500dd412dbafe4403deee16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348570"
---
# <a name="opentnefstreamex"></a><span data-ttu-id="325e7-103">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="325e7-103">OpenTnefStreamEx</span></span>

<span data-ttu-id="325e7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="325e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="325e7-105">Cria um objeto TNEF (Transport-neutral Encapsulation Format) que pode ser usado para codificar ou decodificar um objeto Message em um fluxo de dados TNEF para uso por transportes ou gateways e repositórios de mensagens.</span><span class="sxs-lookup"><span data-stu-id="325e7-105">Creates a Transport-Neutral Encapsulation Format (TNEF) object that can be used to encode or decode a message object into a TNEF data stream for use by transports or gateways and message stores.</span></span> <span data-ttu-id="325e7-106">Este é o ponto de entrada para acesso TNEF.</span><span class="sxs-lookup"><span data-stu-id="325e7-106">This is the entry point for TNEF access.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="325e7-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="325e7-107">Header file:</span></span>  <br/> |<span data-ttu-id="325e7-108">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="325e7-108">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="325e7-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="325e7-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="325e7-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="325e7-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="325e7-111">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="325e7-111">Called by:</span></span>  <br/> |<span data-ttu-id="325e7-112">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="325e7-112">Transport providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="325e7-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="325e7-113">Parameters</span></span>

<span data-ttu-id="325e7-114">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="325e7-114">_lpvSupport_</span></span>
  
> <span data-ttu-id="325e7-115">no Passa um objeto support ou passa NULL.</span><span class="sxs-lookup"><span data-stu-id="325e7-115">[in] Passes a support object, or passes in NULL.</span></span> <span data-ttu-id="325e7-116">Se NULL, o parâmetro _lpAddressBook_ deve ser não nulo.</span><span class="sxs-lookup"><span data-stu-id="325e7-116">If NULL, the  _lpAddressBook_ parameter should be non-null.</span></span> 
    
<span data-ttu-id="325e7-117">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="325e7-117">_lpStream_</span></span>
  
> <span data-ttu-id="325e7-118">no Ponteiro para um objeto de fluxo de armazenamento, como uma interface de **IStream** OLE, fornecendo uma origem ou um destino para uma mensagem de fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="325e7-118">[in] Pointer to a storage stream object, such as an OLE **IStream** interface, providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="325e7-119">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="325e7-119">_lpszStreamName_</span></span>
  
> <span data-ttu-id="325e7-120">no Ponteiro para o nome do fluxo de dados que o objeto TNEF usa.</span><span class="sxs-lookup"><span data-stu-id="325e7-120">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="325e7-121">Se o chamador tiver definido o sinalizador TNEF_ENCODE (parâmetro _parâmetroulflags_ ) em sua chamada para **OpenTnefStream**, o parâmetro _lpszName_ deverá especificar um ponteiro não nulo para uma cadeia de caracteres não nula que consista em qualquer caractere considerado válido para nomear um arquivo.</span><span class="sxs-lookup"><span data-stu-id="325e7-121">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="325e7-122">O MAPI não permite nomes de cadeia de caracteres, incluindo os caracteres "[", "]" ou ":", mesmo se o sistema de arquivos permitir seu uso.</span><span class="sxs-lookup"><span data-stu-id="325e7-122">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="325e7-123">O tamanho da cadeia de caracteres passada para o parâmetro _lpszName_ não deve exceder o valor de MAX_PATH, o tamanho máximo de uma cadeia de caracteres que contém um nome de caminho.</span><span class="sxs-lookup"><span data-stu-id="325e7-123">The size of the string passed for the  _lpszName_ parameter must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="325e7-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="325e7-124">_ulFlags_</span></span>
  
> <span data-ttu-id="325e7-125">no Bitmask dos sinalizadores usados para indicar o modo da função.</span><span class="sxs-lookup"><span data-stu-id="325e7-125">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="325e7-126">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="325e7-126">The following flags can be set:</span></span>
    
<span data-ttu-id="325e7-127">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="325e7-127">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="325e7-128">Todas as propriedades possíveis são mapeadas em seus atributos de nível inferior, mas quando há uma possível perda de dados devido à conversão em um atributo de nível inferior, a propriedade também é codificada nos encapsulamentos.</span><span class="sxs-lookup"><span data-stu-id="325e7-128">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="325e7-129">Observe que isso causará a duplicação de informações no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="325e7-129">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="325e7-130">TNEF_BEST_DATA é o padrão se nenhum outro modo for especificado.</span><span class="sxs-lookup"><span data-stu-id="325e7-130">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="325e7-131">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="325e7-131">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="325e7-132">Fornece compatibilidade com aplicativos cliente mais antigos.</span><span class="sxs-lookup"><span data-stu-id="325e7-132">Provides backward compatibility with older client applications.</span></span> <span data-ttu-id="325e7-133">Os fluxos TNEF codificados com esse sinalizador mapearão todas as propriedades possíveis para o atributo de nível inferior correspondente.</span><span class="sxs-lookup"><span data-stu-id="325e7-133">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="325e7-134">Esse modo também faz com que o padrão de algumas propriedades exigidas por clientes de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="325e7-134">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="325e7-135">Este sinalizador é obsoleto e não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="325e7-135">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="325e7-136">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="325e7-136">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="325e7-137">O objeto TNEF no fluxo indicado é aberto com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="325e7-137">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="325e7-138">O provedor de transporte deve definir esse sinalizador se a função for inicializar o objeto para decodificação subsequente.</span><span class="sxs-lookup"><span data-stu-id="325e7-138">The transport provider must set this flag if the function is to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="325e7-139">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="325e7-139">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="325e7-140">O objeto TNEF no fluxo indicado é aberto para permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="325e7-140">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="325e7-141">O provedor de transporte deve definir esse sinalizador se a função for inicializar o objeto para a codificação subsequente.</span><span class="sxs-lookup"><span data-stu-id="325e7-141">The transport provider must set this flag if the function is to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="325e7-142">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="325e7-142">TNEF_PURE</span></span> 
  
> <span data-ttu-id="325e7-143">Codifica todas as propriedades nos blocos de encapsulamento MAPI.</span><span class="sxs-lookup"><span data-stu-id="325e7-143">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="325e7-144">Portanto, um arquivo TNEF "puro" será composto de, no máximo, os atributos attMAPIProps, attAttachment, attRenddata e attRecipTable.</span><span class="sxs-lookup"><span data-stu-id="325e7-144">Therefore, a "pure" TNEF file will consist of, at most, the attributes attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="325e7-145">Esse modo é ideal para uso quando não é necessária nenhuma compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="325e7-145">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="325e7-146">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="325e7-146">_lpMessage_</span></span>
  
> <span data-ttu-id="325e7-147">no Ponteiro para um objeto Message como um destino para uma mensagem decodificada com anexos ou uma fonte para uma mensagem codificada com anexos.</span><span class="sxs-lookup"><span data-stu-id="325e7-147">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="325e7-148">Todas as propriedades de uma mensagem de destino podem ser substituídas pelas propriedades de uma mensagem codificada.</span><span class="sxs-lookup"><span data-stu-id="325e7-148">Any properties of a destination message can be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="325e7-149">_wKeyVal_</span><span class="sxs-lookup"><span data-stu-id="325e7-149">_wKeyVal_</span></span>
  
> <span data-ttu-id="325e7-150">no Uma chave de pesquisa que o objeto TNEF usa para corresponder anexos às marcas de texto inseridas no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="325e7-150">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="325e7-151">Esse valor deve ser relativamente exclusivo nas mensagens.</span><span class="sxs-lookup"><span data-stu-id="325e7-151">This value should be relatively unique across messages.</span></span> 
    
<span data-ttu-id="325e7-152">_lpAddressBook_</span><span class="sxs-lookup"><span data-stu-id="325e7-152">_lpAddressBook_</span></span>
  
> <span data-ttu-id="325e7-153">no Ponteiro para um objeto de catálogo de endereços usado para obter informações de endereçamento para identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="325e7-153">[in] Pointer to an address book object used to get addressing information for entry identifiers.</span></span> 
    
<span data-ttu-id="325e7-154">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="325e7-154">_lppTNEF_</span></span>
  
> <span data-ttu-id="325e7-155">bota Ponteiro para o novo objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="325e7-155">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="325e7-156">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="325e7-156">Return value</span></span>

<span data-ttu-id="325e7-157">S_OK</span><span class="sxs-lookup"><span data-stu-id="325e7-157">S_OK</span></span> 
  
> <span data-ttu-id="325e7-158">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="325e7-158">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="325e7-159">Comentários</span><span class="sxs-lookup"><span data-stu-id="325e7-159">Remarks</span></span>

<span data-ttu-id="325e7-160">A função **OpenTnefStreamEx** é a substituição recomendada para o [OpenTnefStream](opentnefstream.md), o ponto de entrada original para acesso TNEF.</span><span class="sxs-lookup"><span data-stu-id="325e7-160">The **OpenTnefStreamEx** function is the recommended replacement for [OpenTnefStream](opentnefstream.md), the original entry point for TNEF access.</span></span> 
  
<span data-ttu-id="325e7-161">Um objeto TNEF criado pela função **OpenTnefStreamEx** , posteriormente, chama o método OLE **IUnknown: AddRef** para adicionar referências para o objeto support, o objeto Stream e o objeto Message.</span><span class="sxs-lookup"><span data-stu-id="325e7-161">A TNEF object created by the **OpenTnefStreamEx** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="325e7-162">O provedor de transporte pode liberar as referências para todos os três objetos com uma única chamada para o método OLE **IUnknown:: Release** no objeto TNEF.</span><span class="sxs-lookup"><span data-stu-id="325e7-162">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="325e7-163">**OpenTnefStreamEx** aloca e inicializa um objeto TNEF para o provedor usar na codificação de uma mensagem MAPI em uma mensagem de fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="325e7-163">**OpenTnefStreamEx** allocates and initializes a TNEF object for the provider to use in encoding a MAPI message into a TNEF stream message.</span></span> <span data-ttu-id="325e7-164">Como alternativa, essa função pode configurar o objeto para o provedor usar em chamadas subsequentes para [ITnef:: ExtractProps](itnef-extractprops.md) para decodificar uma mensagem de fluxo TNEF em uma mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="325e7-164">Alternatively, this function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="325e7-165">Para liberar o objeto TNEF e fechar a sessão, o provedor de transporte deve chamar o método **IUnknown:: Release** herdado no objeto.</span><span class="sxs-lookup"><span data-stu-id="325e7-165">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="325e7-166">O valor base para o parâmetro _wKeyVal_ não deve ser zero e não deve ser o mesmo para todas as chamadas para **OpenTnefStreamEx**.</span><span class="sxs-lookup"><span data-stu-id="325e7-166">The base value for the  _wKeyVal_ parameter must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="325e7-167">Em vez disso, use números aleatórios com base na hora do sistema do gerador de números aleatórios da biblioteca de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="325e7-167">Instead, use random numbers based on the system time from the run-time library's random number generator.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="325e7-168">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="325e7-168">MFCMAPI reference</span></span>

<span data-ttu-id="325e7-169">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="325e7-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="325e7-170">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="325e7-170">**File**</span></span>|<span data-ttu-id="325e7-171">**Função**</span><span class="sxs-lookup"><span data-stu-id="325e7-171">**Function**</span></span>|<span data-ttu-id="325e7-172">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="325e7-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="325e7-173">Arquivo. cpp</span><span class="sxs-lookup"><span data-stu-id="325e7-173">File.cpp</span></span>  <br/> |<span data-ttu-id="325e7-174">LoadFromTNEF</span><span class="sxs-lookup"><span data-stu-id="325e7-174">LoadFromTNEF</span></span>  <br/> |<span data-ttu-id="325e7-175">MFCMAPI usa o método **OpenTnefStreamEx** para abrir um Stream no arquivo TNEF para que as propriedades possam ser extraídas.</span><span class="sxs-lookup"><span data-stu-id="325e7-175">MFCMAPI uses the **OpenTnefStreamEx** method to open a stream on the TNEF file so properties may be extracted.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="325e7-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="325e7-176">See also</span></span>

- [<span data-ttu-id="325e7-177">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="325e7-177">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="325e7-178">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="325e7-178">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="325e7-179">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="325e7-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

