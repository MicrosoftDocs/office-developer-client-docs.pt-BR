---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b05f5b30eceb7df1bed76c64f4bdda87ede0e463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439090"
---
# <a name="openstreamonfile"></a><span data-ttu-id="c0672-103">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="c0672-103">OpenStreamOnFile</span></span>

  
  
<span data-ttu-id="c0672-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0672-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0672-105">Aloca e inicializa um objeto OLE **IStream** para acessar o conteúdo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c0672-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="c0672-106">Essa função usa uma cadeia de caracteres ANSI como o nome do arquivo, incluindo o caminho e a extensão do arquivo, portanto, recomenda-se o uso da versão Unicode dessa função, [OpenStreamOnFileW.](openstreamonfilew.md)</span><span class="sxs-lookup"><span data-stu-id="c0672-106">This function takes an ANSI string as the file name including the path and the file extension, therefore, use of the Unicode version of this function, [OpenStreamOnFileW](openstreamonfilew.md), is recommended.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0672-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c0672-107">Header file:</span></span>  <br/> |<span data-ttu-id="c0672-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c0672-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c0672-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c0672-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="c0672-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="c0672-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="c0672-111">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="c0672-111">Called by:</span></span>  <br/> |<span data-ttu-id="c0672-112">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="c0672-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFile(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPSTR lpszFileName,
  LPSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="c0672-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0672-113">Parameters</span></span>

 <span data-ttu-id="c0672-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="c0672-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="c0672-115">[in] Ponteiro para a [função MAPIAllocateBuffer,](mapiallocatebuffer.md) a ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="c0672-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="c0672-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="c0672-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="c0672-117">[in] Ponteiro para a [função MAPIFreeBuffer,](mapifreebuffer.md) a ser usado para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="c0672-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="c0672-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c0672-118">_ulFlags_</span></span>
  
> <span data-ttu-id="c0672-119">[in] Bitmask de sinalizadores usados para controlar a criação ou abertura do arquivo a ser acessado por meio do objeto **IStream** OLE.</span><span class="sxs-lookup"><span data-stu-id="c0672-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="c0672-120">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="c0672-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="c0672-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="c0672-121">SOF_UNIQUEFILENAME</span></span> 
  
> <span data-ttu-id="c0672-122">Um arquivo temporário deve ser criado para o **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="c0672-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="c0672-123">Se esse sinalizador estiver definido, os sinalizadores STGM_CREATE e STGM_READWRITE também deverão ser definidos.</span><span class="sxs-lookup"><span data-stu-id="c0672-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="c0672-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="c0672-124">STGM_CREATE</span></span> 
  
> <span data-ttu-id="c0672-125">O arquivo deve ser criado mesmo que já exista um.</span><span class="sxs-lookup"><span data-stu-id="c0672-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="c0672-126">Se o  _parâmetro lpszFileName_ não estiver definido, esse sinalizador e STGM_DELETEONRELEASE deverão ser definidos.</span><span class="sxs-lookup"><span data-stu-id="c0672-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="c0672-127">Se STGM_CREATE for definido, o sinalizador STGM_READWRITE também deverá ser definido.</span><span class="sxs-lookup"><span data-stu-id="c0672-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="c0672-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="c0672-128">STGM_DELETEONRELEASE</span></span> 
  
> <span data-ttu-id="c0672-129">O arquivo será excluído quando o objeto **IStream** for liberado.</span><span class="sxs-lookup"><span data-stu-id="c0672-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="c0672-130">Se o  _parâmetro lpszFileName_ não estiver definido, esse sinalizador e STGM_CREATE deverão ser definidos.</span><span class="sxs-lookup"><span data-stu-id="c0672-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="c0672-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="c0672-131">STGM_READ</span></span> 
  
> <span data-ttu-id="c0672-132">O arquivo deve ser criado ou aberto com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c0672-132">The file is to be created or opened with read-only access.</span></span> 
    
<span data-ttu-id="c0672-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="c0672-133">STGM_READWRITE</span></span> 
  
> <span data-ttu-id="c0672-134">O arquivo deve ser criado ou aberto com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c0672-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="c0672-135">Se esse sinalizador não estiver definido, o STGM_CREATE não deverá ser definido.</span><span class="sxs-lookup"><span data-stu-id="c0672-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span> 
    
 <span data-ttu-id="c0672-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="c0672-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="c0672-137">[in] O nome do arquivo, incluindo caminho e extensão, do arquivo para o qual **OpenStreamOnFile** inicializa o **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="c0672-137">[in] The filename, including path and extension, of the file for which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="c0672-138">Se o SOF_UNIQUEFILENAME sinalizador estiver definido,  _lpszFileName_ conterá o caminho para o diretório no qual será criado um arquivo temporário.</span><span class="sxs-lookup"><span data-stu-id="c0672-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="c0672-139">Se  _lpszFileName_ for NULL, **OpenStreamOnFile** obterá um caminho apropriado do sistema, e os sinalizadores STGM_CREATE e STGM_DELETEONRELEASE devem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="c0672-139">If  _lpszFileName_ is NULL, **OpenStreamOnFile** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="c0672-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="c0672-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="c0672-141">[in] O prefixo do nome do arquivo no qual **OpenStreamOnFile** inicializa o **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="c0672-141">[in] The prefix for the filename on which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="c0672-142">Se definido, o prefixo não deve conter mais de três caracteres.</span><span class="sxs-lookup"><span data-stu-id="c0672-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="c0672-143">Se  _lpszPrefix_ for NULL, será usado um prefixo "SOF".</span><span class="sxs-lookup"><span data-stu-id="c0672-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="c0672-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="c0672-144">_lppStream_</span></span>
  
> <span data-ttu-id="c0672-145">[out] Ponteiro para um ponteiro para um objeto expondo a interface **IStream.**</span><span class="sxs-lookup"><span data-stu-id="c0672-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c0672-146">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c0672-146">Return value</span></span>

<span data-ttu-id="c0672-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0672-147">S_OK</span></span> 
  
> <span data-ttu-id="c0672-148">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="c0672-148">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="c0672-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c0672-149">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c0672-150">O arquivo não pôde ser acessado devido a permissões de usuário insuficientes ou porque arquivos somente leitura não podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="c0672-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span> 
    
<span data-ttu-id="c0672-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c0672-151">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c0672-152">O arquivo designado não existe.</span><span class="sxs-lookup"><span data-stu-id="c0672-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0672-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0672-153">Remarks</span></span>

<span data-ttu-id="c0672-154">A **função OpenStreamOnFile** tem dois usos importantes, diferenciados pela configuração do sinalizador SOF_UNIQUEFILENAME função.</span><span class="sxs-lookup"><span data-stu-id="c0672-154">The **OpenStreamOnFile** function has two important uses, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="c0672-155">Quando esse sinalizador não está definido, **OpenStreamOnFile** abre um objeto **IStream** em um arquivo existente, por exemplo, para copiar seu conteúdo para a propriedade **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de um anexo usando o método **IStream::CopyTo.**</span><span class="sxs-lookup"><span data-stu-id="c0672-155">When this flag is not set, **OpenStreamOnFile** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="c0672-156">Nesse caso, o  _parâmetro lpszFileName_ especifica o caminho e o nome de arquivo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c0672-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="c0672-157">Quando SOF_UNIQUEFILENAME é definido, **o OpenStreamOnFile** cria um arquivo temporário para manter os dados de **um objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="c0672-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFile** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="c0672-158">Para esse uso, o parâmetro  _lpszFileName_ pode, opcionalmente, designar o caminho para o diretório onde o arquivo deve ser criado, e o parâmetro  _lpszPrefix_ pode, opcionalmente, especificar um prefixo para o nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c0672-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="c0672-159">Quando o aplicativo cliente ou provedor de serviços de chamada for concluído com o objeto **IStream,** ele deverá liberá-lo chamando o método **OLE IStream::Release.**</span><span class="sxs-lookup"><span data-stu-id="c0672-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="c0672-160">MAPI uses the functions pointed to  _by lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="c0672-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c0672-161">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="c0672-161">Notes to callers</span></span>

<span data-ttu-id="c0672-162">O SOF_UNIQUEFILENAME sinalizador é usado para criar um arquivo temporário com um nome exclusivo para o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c0672-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="c0672-163">Se esse sinalizador estiver definido, o parâmetro  _lpszFileName_ especifica o caminho do arquivo temporário e o parâmetro  _lpszPrefix_ contém os caracteres de prefixo do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c0672-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="c0672-164">O nome de arquivo construído é <prefix> HHHH. TMP, onde HHHH é um número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="c0672-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="c0672-165">Se  _lpszFileName_ for NULL, o arquivo será criado no diretório de arquivos temporários retornado da função **Windows GetTempPath** ou no diretório atual se nenhum diretório de arquivos temporário tiver sido designado.</span><span class="sxs-lookup"><span data-stu-id="c0672-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span> 
  
<span data-ttu-id="c0672-166">Se o sinalizador SOF_UNIQUEFILENAME não estiver definido,  _lpszPrefix_ será ignorado e  _lpszFileName_ deverá conter o caminho totalmente qualificado e o nome de arquivo do arquivo a ser aberto ou criado.</span><span class="sxs-lookup"><span data-stu-id="c0672-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="c0672-167">O arquivo será aberto ou criado com base nos outros sinalizadores definidos em _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="c0672-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c0672-168">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c0672-168">MFCMAPI reference</span></span>

<span data-ttu-id="c0672-169">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0672-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c0672-170">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="c0672-170">**File**</span></span>|<span data-ttu-id="c0672-171">**Função**</span><span class="sxs-lookup"><span data-stu-id="c0672-171">**Function**</span></span>|<span data-ttu-id="c0672-172">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="c0672-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c0672-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="c0672-173">File.cpp</span></span>  <br/> |<span data-ttu-id="c0672-174">WriteAttachStreamToFile</span><span class="sxs-lookup"><span data-stu-id="c0672-174">WriteAttachStreamToFile</span></span>  <br/> |<span data-ttu-id="c0672-175">MFCMAPI usa o **método OpenStreamOnFile** para abrir um fluxo em um arquivo para que um anexo possa ser gravado nele.</span><span class="sxs-lookup"><span data-stu-id="c0672-175">MFCMAPI uses the **OpenStreamOnFile** method to open a stream on a file so an attachment can be written out to it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0672-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0672-176">See also</span></span>



[<span data-ttu-id="c0672-177">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="c0672-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

