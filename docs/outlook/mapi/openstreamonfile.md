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
ms.openlocfilehash: 8c246968dcac719a8ee8177e20e802f9c7033435
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768193"
---
# <a name="openstreamonfile"></a><span data-ttu-id="21e40-103">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="21e40-103">OpenStreamOnFile</span></span>

  
  
<span data-ttu-id="21e40-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="21e40-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="21e40-105">Aloca e inicializa um objeto OLE **IStream** para acessar o conteúdo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="21e40-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="21e40-106">Essa função usa uma sequência de caracteres ANSI, como o nome de arquivo, incluindo o caminho e a extensão de arquivo, portanto, o uso da versão Unicode dessa função, [OpenStreamOnFileW](openstreamonfilew.md), é recomendado.</span><span class="sxs-lookup"><span data-stu-id="21e40-106">This function takes an ANSI string as the file name including the path and the file extension, therefore, use of the Unicode version of this function, [OpenStreamOnFileW](openstreamonfilew.md), is recommended.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="21e40-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="21e40-107">Header file:</span></span>  <br/> |<span data-ttu-id="21e40-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="21e40-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="21e40-109">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="21e40-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="21e40-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="21e40-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="21e40-111">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="21e40-111">Called by:</span></span>  <br/> |<span data-ttu-id="21e40-112">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="21e40-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="21e40-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21e40-113">Parameters</span></span>

 <span data-ttu-id="21e40-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="21e40-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="21e40-115">[in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="21e40-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="21e40-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="21e40-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="21e40-117">[in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="21e40-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="21e40-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="21e40-118">_ulFlags_</span></span>
  
> <span data-ttu-id="21e40-119">[in] Bitmask dos sinalizadores usados para controlar a criação ou a abertura do arquivo a ser acessado através do objeto OLE **IStream** .</span><span class="sxs-lookup"><span data-stu-id="21e40-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="21e40-120">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="21e40-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="21e40-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="21e40-121">SOF_UNIQUEFILENAME</span></span> 
  
> <span data-ttu-id="21e40-122">Um arquivo temporário deve ser criada para o objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="21e40-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="21e40-123">Se esse sinalizador estiver definido, os sinalizadores STGM_CREATE e STGM_READWRITE também devem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="21e40-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="21e40-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="21e40-124">STGM_CREATE</span></span> 
  
> <span data-ttu-id="21e40-125">O arquivo deve ser criada, mesmo se já existir.</span><span class="sxs-lookup"><span data-stu-id="21e40-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="21e40-126">Se o parâmetro _lpszFileName_ não estiver definido, esse sinalizador e o STGM_DELETEONRELEASE devem ser definida.</span><span class="sxs-lookup"><span data-stu-id="21e40-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="21e40-127">Se STGM_CREATE for definido, o sinalizador STGM_READWRITE também deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="21e40-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="21e40-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="21e40-128">STGM_DELETEONRELEASE</span></span> 
  
> <span data-ttu-id="21e40-129">O arquivo deve ser excluído quando o objeto **IStream** for lançado.</span><span class="sxs-lookup"><span data-stu-id="21e40-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="21e40-130">Se o parâmetro _lpszFileName_ não estiver definido, esse sinalizador e o STGM_CREATE devem ser definida.</span><span class="sxs-lookup"><span data-stu-id="21e40-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="21e40-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="21e40-131">STGM_READ</span></span> 
  
> <span data-ttu-id="21e40-132">O arquivo deve ser criada ou aberta com acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="21e40-132">The file is to be created or opened with read-only access.</span></span> 
    
<span data-ttu-id="21e40-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="21e40-133">STGM_READWRITE</span></span> 
  
> <span data-ttu-id="21e40-134">O arquivo deve ser criado ou aberto com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="21e40-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="21e40-135">Se esse sinalizador não estiver definida, o sinalizador STGM_CREATE não deve ser definido uma.</span><span class="sxs-lookup"><span data-stu-id="21e40-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span> 
    
 <span data-ttu-id="21e40-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="21e40-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="21e40-137">[in] O nome de arquivo, incluindo o caminho e a extensão, do arquivo para o qual **OpenStreamOnFile** inicializa o objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="21e40-137">[in] The filename, including path and extension, of the file for which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="21e40-138">Se o sinalizador SOF_UNIQUEFILENAME estiver definido, _lpszFileName_ contém o caminho para o diretório no qual deseja criar um arquivo temporário.</span><span class="sxs-lookup"><span data-stu-id="21e40-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="21e40-139">Se _lpszFileName_ for NULL, **OpenStreamOnFile** obtém um caminho adequado do sistema e os STGM_CREATE STGM_DELETEONRELEASE sinalizadores e devem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="21e40-139">If  _lpszFileName_ is NULL, **OpenStreamOnFile** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="21e40-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="21e40-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="21e40-141">[in] O prefixo para o nome de arquivo no qual **OpenStreamOnFile** inicializa o objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="21e40-141">[in] The prefix for the filename on which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="21e40-142">Se definido, o prefixo deve conter não mais de três caracteres.</span><span class="sxs-lookup"><span data-stu-id="21e40-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="21e40-143">Se _lpszPrefix_ for NULL, um prefixo de "SOF" é usado.</span><span class="sxs-lookup"><span data-stu-id="21e40-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="21e40-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="21e40-144">_lppStream_</span></span>
  
> <span data-ttu-id="21e40-145">[out] Ponteiro para um ponteiro para um objeto expondo a interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="21e40-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="21e40-146">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="21e40-146">Return value</span></span>

<span data-ttu-id="21e40-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="21e40-147">S_OK</span></span> 
  
> <span data-ttu-id="21e40-148">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="21e40-148">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="21e40-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="21e40-149">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="21e40-150">O arquivo não pôde ser acessado devido a permissões insuficientes do usuário ou porque os arquivos somente leitura não podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="21e40-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span> 
    
<span data-ttu-id="21e40-151">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="21e40-151">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="21e40-152">O arquivo designado não existe.</span><span class="sxs-lookup"><span data-stu-id="21e40-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21e40-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="21e40-153">Remarks</span></span>

<span data-ttu-id="21e40-154">A função **OpenStreamOnFile** tem dois usos importantes, diferenciados pela definição do sinalizador SOF_UNIQUEFILENAME.</span><span class="sxs-lookup"><span data-stu-id="21e40-154">The **OpenStreamOnFile** function has two important uses, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="21e40-155">Quando esse sinalizador não estiver definida, **OpenStreamOnFile** abre um objeto **IStream** em um arquivo existente, por exemplo, para copiar o conteúdo à propriedade **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de um anexo usando o **IStream :: CopyTo** método.</span><span class="sxs-lookup"><span data-stu-id="21e40-155">When this flag is not set, **OpenStreamOnFile** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="21e40-156">Nesse caso, o parâmetro _lpszFileName_ Especifica o caminho e o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="21e40-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="21e40-157">Quando SOF_UNIQUEFILENAME estiver definido, **OpenStreamOnFile** cria um arquivo temporário para armazenar dados para um objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="21e40-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFile** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="21e40-158">Para este uso, o parâmetro _lpszFileName_ opcionalmente pode designar o caminho para o diretório onde o arquivo deve ser criada, e o parâmetro _lpszPrefix_ , opcionalmente, pode especificar um prefixo para o nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="21e40-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="21e40-159">Quando o aplicativo de cliente chamada ou o provedor de serviço for concluído com o objeto **IStream** , ele deve liberá-la ao chamar o método OLE **IStream::Release** .</span><span class="sxs-lookup"><span data-stu-id="21e40-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="21e40-160">O MAPI usa as funções apontadas pela _lpAllocateBuffer_ e _lpFreeBuffer_ para a maioria dos alocação de memória e desalocação, especificamente para alocar memória para uso por aplicativos do cliente, ao chamar interfaces de objeto, como [IMAPIProp:: GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="21e40-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="21e40-161">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="21e40-161">Notes to callers</span></span>

<span data-ttu-id="21e40-162">O sinalizador SOF_UNIQUEFILENAME é usado para criar um arquivo temporário com um nome exclusivo para o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="21e40-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="21e40-163">Se esse sinalizador estiver definido, a parâmetro de _lpszFileName_ Especifica o caminho para o arquivo temporário e o parâmetro _lpszPrefix_ contém os caracteres de prefixo do nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="21e40-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="21e40-164">É o nome de arquivo criado <prefix>HHHH. TMP, onde HHHH é um número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="21e40-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="21e40-165">Se _lpszFileName_ for NULL, o arquivo será criado no diretório atual ou o diretório de arquivo temporário que é retornado da função Windows **GetTempPath**se nenhuma diretório de arquivos temporários foi designado.</span><span class="sxs-lookup"><span data-stu-id="21e40-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span> 
  
<span data-ttu-id="21e40-166">Se o sinalizador SOF_UNIQUEFILENAME não estiver definido, _lpszPrefix_ será ignorado e _lpszFileName_ deve conter o caminho totalmente qualificado e o nome do arquivo a ser aberto ou criado.</span><span class="sxs-lookup"><span data-stu-id="21e40-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="21e40-167">O arquivo será aberto ou criado com base em outros sinalizadores que são definidos na _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="21e40-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="21e40-168">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="21e40-168">MFCMAPI reference</span></span>

<span data-ttu-id="21e40-169">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="21e40-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="21e40-170">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="21e40-170">**File**</span></span>|<span data-ttu-id="21e40-171">**Function**</span><span class="sxs-lookup"><span data-stu-id="21e40-171">**Function**</span></span>|<span data-ttu-id="21e40-172">**Comment**</span><span class="sxs-lookup"><span data-stu-id="21e40-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="21e40-173">CPP</span><span class="sxs-lookup"><span data-stu-id="21e40-173">File.cpp</span></span>  <br/> |<span data-ttu-id="21e40-174">WriteAttachStreamToFile</span><span class="sxs-lookup"><span data-stu-id="21e40-174">WriteAttachStreamToFile</span></span>  <br/> |<span data-ttu-id="21e40-175">MFCMAPI usa o método **OpenStreamOnFile** para abrir um stream em um arquivo, de forma que um anexo pode ser gravado em-lo.</span><span class="sxs-lookup"><span data-stu-id="21e40-175">MFCMAPI uses the **OpenStreamOnFile** method to open a stream on a file so an attachment can be written out to it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21e40-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="21e40-176">See also</span></span>



[<span data-ttu-id="21e40-177">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="21e40-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

