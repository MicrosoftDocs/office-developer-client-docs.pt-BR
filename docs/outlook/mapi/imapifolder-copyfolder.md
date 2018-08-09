---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5961e7a2118a46bdc9c0e66138363976ae2f7154
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766969"
---
# <a name="imapifoldercopyfolder"></a><span data-ttu-id="c019e-103">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="c019e-103">IMAPIFolder::CopyFolder</span></span>

  
  
<span data-ttu-id="c019e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c019e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c019e-105">Copia ou move uma subpasta.</span><span class="sxs-lookup"><span data-stu-id="c019e-105">Copies or moves a subfolder.</span></span>
  
```cpp
HRESULT CopyFolder(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  LPSTR lpszNewFolderName,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c019e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c019e-106">Parameters</span></span>

 <span data-ttu-id="c019e-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c019e-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="c019e-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="c019e-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c019e-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c019e-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="c019e-110">[in] Um ponteiro para o identificador de entrada da subpasta para copiar ou mover.</span><span class="sxs-lookup"><span data-stu-id="c019e-110">[in] A pointer to the entry identifier of the subfolder to copy or move.</span></span>
    
 <span data-ttu-id="c019e-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c019e-111">_lpInterface_</span></span>
  
> <span data-ttu-id="c019e-112">[in] Um ponteiro para o identificador de interface (IID) que representa a ser usado para acessar a pasta em que o parâmetro _lpDestFolder_ aponta para a interface.</span><span class="sxs-lookup"><span data-stu-id="c019e-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that the  _lpDestFolder_ parameter points to.</span></span> <span data-ttu-id="c019e-113">Passar NULL faz com que o provedor de serviços retornar a interface de pasta padrão, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="c019e-113">Passing NULL causes the service provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="c019e-114">Os valores válidos para _lpInterface_ incluem IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer e IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="c019e-114">Valid values for  _lpInterface_ include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="c019e-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="c019e-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="c019e-116">[in] Um ponteiro para a pasta aberta para receber a subpasta copiada ou movida.</span><span class="sxs-lookup"><span data-stu-id="c019e-116">[in] A pointer to the open folder to receive the copied or moved subfolder.</span></span>
    
 <span data-ttu-id="c019e-117">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="c019e-117">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="c019e-118">[in] Um ponteiro para o nome da pasta no seu novo destino copiado ou movido.</span><span class="sxs-lookup"><span data-stu-id="c019e-118">[in] A pointer to the name of the copied or moved folder in its new destination.</span></span> <span data-ttu-id="c019e-119">Se _lpszNewFolderName_ for definido como NULL, o nome da subpasta fonte é usado para o nome da pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="c019e-119">If  _lpszNewFolderName_ is set to NULL, the name of the source subfolder is used for the name of the destination folder.</span></span> 
    
 <span data-ttu-id="c019e-120">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c019e-120">_ulUIParam_</span></span>
  
> <span data-ttu-id="c019e-121">[in] Um identificador para a janela pai do indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="c019e-121">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="c019e-122">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador FOLDER_DIALOG no parâmetro _ulFlags_ está definido.</span><span class="sxs-lookup"><span data-stu-id="c019e-122">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag in the  _ulFlags_ parameter is set.</span></span> 
    
 <span data-ttu-id="c019e-123">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="c019e-123">_lpProgress_</span></span>
  
> <span data-ttu-id="c019e-124">[in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="c019e-124">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="c019e-125">Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="c019e-125">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="c019e-126">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG está definido na _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="c019e-126">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="c019e-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c019e-127">_ulFlags_</span></span>
  
> <span data-ttu-id="c019e-128">[in] Uma bitmask dos sinalizadores que controla a operação de cópia ou movimentação.</span><span class="sxs-lookup"><span data-stu-id="c019e-128">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="c019e-129">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="c019e-129">The following flags can be set:</span></span>
    
<span data-ttu-id="c019e-130">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="c019e-130">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="c019e-131">Todas as subpastas na subpasta a ser copiado também devem ser copiadas.</span><span class="sxs-lookup"><span data-stu-id="c019e-131">All of the subfolders in the subfolder to be copied should also be copied.</span></span> <span data-ttu-id="c019e-132">Quando COPY_SUBFOLDERS não estiver definida para uma operação de cópia, somente a subpasta identificada pela _lpEntryID_ é copiada.</span><span class="sxs-lookup"><span data-stu-id="c019e-132">When COPY_SUBFOLDERS is not set for a copy operation, only the subfolder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="c019e-133">Com uma operação de movimentação, o comportamento COPY_SUBFOLDERS é o padrão independentemente se o sinalizador está definido.</span><span class="sxs-lookup"><span data-stu-id="c019e-133">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="c019e-134">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c019e-134">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="c019e-135">Solicita a exibição de um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="c019e-135">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="c019e-136">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="c019e-136">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="c019e-137">A subpasta deve ser movido, em vez de copiados.</span><span class="sxs-lookup"><span data-stu-id="c019e-137">The subfolder is to be moved instead of copied.</span></span> <span data-ttu-id="c019e-138">Se FOLDER_MOVE não estiver definida, a subpasta será copiada.</span><span class="sxs-lookup"><span data-stu-id="c019e-138">If FOLDER_MOVE is not set, the subfolder is copied.</span></span>
    
<span data-ttu-id="c019e-139">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="c019e-139">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="c019e-140">Informa que o provedor de armazenamento de mensagem que se ele implementa **CopyFolder** chamando o método do objeto seu suporte de [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) ou [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) , **CopyFolder** deve em vez disso imediatamente retornar MAPI_E_ DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="c019e-140">Informs the message store provider that if it implements **CopyFolder** by calling its support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method, **CopyFolder** should instead immediately return MAPI_E_DECLINE_COPY.</span></span> 
    
<span data-ttu-id="c019e-141">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c019e-141">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c019e-142">O nome da pasta de destino está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="c019e-142">The name of the destination folder is in Unicode format.</span></span> <span data-ttu-id="c019e-143">Se o sinalizador MAPI_UNICODE não estiver definido, o nome da pasta é no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="c019e-143">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c019e-144">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c019e-144">Return value</span></span>

<span data-ttu-id="c019e-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="c019e-145">S_OK</span></span> 
  
> <span data-ttu-id="c019e-146">A pasta especificada foi copiada ou movida com êxito.</span><span class="sxs-lookup"><span data-stu-id="c019e-146">The specified folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="c019e-147">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c019e-147">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c019e-148">Tanto o sinalizador MAPI_UNICODE foi definido e o provedor de armazenamento de mensagem não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e o provedor de armazenamento de mensagem suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="c019e-148">Either the MAPI_UNICODE flag was set and the message store provider does not support Unicode, or MAPI_UNICODE was not set and the message store provider supports only Unicode.</span></span>
    
<span data-ttu-id="c019e-149">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="c019e-149">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="c019e-150">O nome da pasta que está sendo movido ou copiadas é igual de uma subpasta na pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="c019e-150">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="c019e-151">O provedor de armazenamento de mensagem requer nomes de pasta exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c019e-151">The message store provider requires unique folder names.</span></span>
    
<span data-ttu-id="c019e-152">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="c019e-152">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="c019e-153">O provedor implemente esse método chamando um método de objeto de suporte e o chamador passou o sinalizador MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="c019e-153">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="c019e-154">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="c019e-154">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="c019e-155">A pasta de origem direta ou indiretamente contém a pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="c019e-155">The source folder directly or indirectly contains the destination folder.</span></span> <span data-ttu-id="c019e-156">Significantes de trabalho talvez tenham sido realizadas antes que esta condição foi descoberta, para a pasta de origem e destino pode ser modificada parcialmente.</span><span class="sxs-lookup"><span data-stu-id="c019e-156">Significant work may have been performed before this condition was discovered, so the source and destination folder may be partially modified.</span></span> 
    
<span data-ttu-id="c019e-157">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="c019e-157">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="c019e-158">A chamada foi bem-sucedida, mas nem todas as entradas foram copiadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="c019e-158">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="c019e-159">Quando esse aviso é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="c019e-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="c019e-160">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="c019e-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="c019e-161">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="c019e-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c019e-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="c019e-162">Remarks</span></span>

<span data-ttu-id="c019e-163">O método **IMAPIFolder::CopyFolder** copia ou move uma subpasta de um local para outro.</span><span class="sxs-lookup"><span data-stu-id="c019e-163">The **IMAPIFolder::CopyFolder** method copies or moves a subfolder from one location to another.</span></span> <span data-ttu-id="c019e-164">A subpasta a ser copiado ou movido é adicionada à pasta de destino como uma subpasta.</span><span class="sxs-lookup"><span data-stu-id="c019e-164">The subfolder being copied or moved is added to the destination folder as a subfolder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c019e-165">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="c019e-165">Notes to implementers</span></span>

<span data-ttu-id="c019e-166">Quando a operação de cópia ou movimentação envolve mais de uma pasta, conforme indicado, definindo o sinalizador COPY_SUBFOLDERS, execute a operação como completamente para cada pasta.</span><span class="sxs-lookup"><span data-stu-id="c019e-166">When the copy or move operation involves more than one folder, as indicated by setting the COPY_SUBFOLDERS flag, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="c019e-167">Em alguns casos, uma das pastas a ser movido ou copiadas não existe ou já foi mudou ou copiada em outros lugares.</span><span class="sxs-lookup"><span data-stu-id="c019e-167">Sometimes one of the folders to be moved or copied does not exist or has already been moved or copied elsewhere.</span></span> <span data-ttu-id="c019e-168">Não interrompa a operação prematuramente, a menos que ocorre uma falha que está fora de seu controle, como ficando sem memória, ficando sem espaço em disco ou corrupção no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c019e-168">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="c019e-169">Tente reter todos os identificadores de entrada de mensagem nas mensagens copiadas.</span><span class="sxs-lookup"><span data-stu-id="c019e-169">Try to retain all message entry identifiers in the copied messages.</span></span> <span data-ttu-id="c019e-170">Você também deve tentar preservar os identificadores de entrada, mas ela não é necessária.</span><span class="sxs-lookup"><span data-stu-id="c019e-170">You should also try to preserve entry identifiers, but it is not required.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c019e-171">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="c019e-171">Notes to callers</span></span>

<span data-ttu-id="c019e-172">Espera esses valores de retorno sob as condições a seguintes.</span><span class="sxs-lookup"><span data-stu-id="c019e-172">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="c019e-173">**Condição**</span><span class="sxs-lookup"><span data-stu-id="c019e-173">**Condition**</span></span>|<span data-ttu-id="c019e-174">**Valor retornado**</span><span class="sxs-lookup"><span data-stu-id="c019e-174">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c019e-175">**CopyFolder** tem copiados ou movidos de cada mensagem e a subpasta com êxito.</span><span class="sxs-lookup"><span data-stu-id="c019e-175">**CopyFolder** has successfully copied or moved every message and subfolder.</span></span>  <br/> |<span data-ttu-id="c019e-176">S_OK</span><span class="sxs-lookup"><span data-stu-id="c019e-176">S_OK</span></span>  <br/> |
|<span data-ttu-id="c019e-177">**CopyFolder** foi capaz de copiar ou mover cada mensagem e a subpasta com êxito.</span><span class="sxs-lookup"><span data-stu-id="c019e-177">**CopyFolder** was unable to successfully copy or move every message and subfolder.</span></span>  <br/> |<span data-ttu-id="c019e-178">MAPI_W_PARTIAL_COMPLETION ou E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c019e-178">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="c019e-179">**CopyFolder** não pôde concluir.</span><span class="sxs-lookup"><span data-stu-id="c019e-179">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="c019e-180">Qualquer valor de erro, exceto E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c019e-180">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="c019e-181">Quando **CopyFolder** é impossível concluir, não presuma que foi feito nenhum trabalho.</span><span class="sxs-lookup"><span data-stu-id="c019e-181">When **CopyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="c019e-182">**CopyFolder** podem ter sido capaz de copiar ou mover um ou mais das mensagens e subpastas antes da ocorrência de erro.</span><span class="sxs-lookup"><span data-stu-id="c019e-182">**CopyFolder** might have been able to copy or move one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="c019e-183">Se um identificador de entrada para uma pasta que não existe é passado _lpEntryID_, **CopyFolder** retorna MAPI_W_PARTIAL_COMPLETION ou E_NOT_FOUND, dependendo da implementação do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c019e-183">If an entry identifier for a folder that does not exist is passed in  _lpEntryID_, **CopyFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
<span data-ttu-id="c019e-184">Dependendo do provedor de repositório de mensagem, o identificador de entrada da mensagem original pode ou não pode ser preservado na mensagem copiada.</span><span class="sxs-lookup"><span data-stu-id="c019e-184">Depending on the message store provider, the entry identifier of the original message may or may not be preserved in the copied message.</span></span> <span data-ttu-id="c019e-185">Você deve preservar os identificadores de entrada sempre que possível, mas não é um requisito.</span><span class="sxs-lookup"><span data-stu-id="c019e-185">You should preserve entry identifiers whenever possible, but it is not a requirement.</span></span> <span data-ttu-id="c019e-186">Geralmente, você pode depender os seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="c019e-186">You can generally depend on the following scenarios:</span></span>
  
- <span data-ttu-id="c019e-187">Quando você move uma pasta entre dois tipos diferentes de repositórios de mensagem, o identificador de entrada é garantido para alterar.</span><span class="sxs-lookup"><span data-stu-id="c019e-187">When you move a folder between two different types of message stores, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="c019e-188">Quando você move uma pasta entre dois armazenamentos de mensagem do mesmo tipo, o identificador de entrada quase sempre é alterado.</span><span class="sxs-lookup"><span data-stu-id="c019e-188">When you move a folder between two message stores of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="c019e-189">Quando você move uma pasta para outro local no repositório de mensagem do mesmo, o identificador de entrada podem ou talvez não alterar, dependendo da mensagem o provedor de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c019e-189">When you move a folder to another location in the same message store, the entry identifier may or may not change, depending on the message store provider.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="c019e-190">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c019e-190">MFCMAPI reference</span></span>

<span data-ttu-id="c019e-191">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c019e-191">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c019e-192">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="c019e-192">**File**</span></span>|<span data-ttu-id="c019e-193">**Function**</span><span class="sxs-lookup"><span data-stu-id="c019e-193">**Function**</span></span>|<span data-ttu-id="c019e-194">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c019e-194">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c019e-195">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c019e-195">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="c019e-196">CMsgStoreDlg::OnPasteFolder</span><span class="sxs-lookup"><span data-stu-id="c019e-196">CMsgStoreDlg::OnPasteFolder</span></span>  <br/> |<span data-ttu-id="c019e-197">MFCMAPI usa o método **IMAPIFolder::CopyFolder** para copiar pastas de um local para outro.</span><span class="sxs-lookup"><span data-stu-id="c019e-197">MFCMAPI uses the **IMAPIFolder::CopyFolder** method to copy folders from one location to another.</span></span> <span data-ttu-id="c019e-198">MFCMAPI se lembra da pasta de origem durante a operação de cópia e realmente executa a cópia durante a operação de colar.</span><span class="sxs-lookup"><span data-stu-id="c019e-198">MFCMAPI remembers the source folder during the copy operation and actually performs the copy during the paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c019e-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="c019e-199">See also</span></span>



[<span data-ttu-id="c019e-200">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c019e-200">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="c019e-201">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="c019e-201">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

