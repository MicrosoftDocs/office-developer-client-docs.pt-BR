---
title: IMAPISupportCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyFolder
api_type:
- COM
ms.assetid: c2e0939f-0668-473f-856c-a27af094070b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 11ee944a14f8c9bd881b9c79a4ce66817275e73a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420882"
---
# <a name="imapisupportcopyfolder"></a><span data-ttu-id="8de3a-103">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="8de3a-103">IMAPISupport::CopyFolder</span></span>

  
  
<span data-ttu-id="8de3a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8de3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8de3a-105">Copia ou move uma pasta da pasta pai atual para outra pasta pai.</span><span class="sxs-lookup"><span data-stu-id="8de3a-105">Copies or moves a folder from its current parent folder to another parent folder.</span></span>
  
```cpp
HRESULT CopyFolder(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
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

## <a name="parameters"></a><span data-ttu-id="8de3a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8de3a-106">Parameters</span></span>

 <span data-ttu-id="8de3a-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="8de3a-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="8de3a-108">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a pasta pai da pasta a ser copiada ou movida.</span><span class="sxs-lookup"><span data-stu-id="8de3a-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the parent folder of the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="8de3a-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="8de3a-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="8de3a-110">no Um ponteiro para a pasta pai da pasta a ser copiada ou movida.</span><span class="sxs-lookup"><span data-stu-id="8de3a-110">[in] A pointer to the parent folder of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="8de3a-111">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="8de3a-111">_cbEntryID_</span></span>
  
> <span data-ttu-id="8de3a-112">no A contagem de bytes no identificador de entrada apontado por _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="8de3a-112">[in] The byte count in the entry identifier pointed to by  _lpEntryID_.</span></span>
    
 <span data-ttu-id="8de3a-113">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="8de3a-113">_lpEntryID_</span></span>
  
> <span data-ttu-id="8de3a-114">no Um ponteiro para o identificador de entrada da pasta a ser copiado ou movido.</span><span class="sxs-lookup"><span data-stu-id="8de3a-114">[in] A pointer to the entry identifier of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="8de3a-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8de3a-115">_lpInterface_</span></span>
  
> <span data-ttu-id="8de3a-116">no Serve deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="8de3a-116">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="8de3a-117">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="8de3a-117">_lpDestFolder_</span></span>
  
> <span data-ttu-id="8de3a-118">no Um ponteiro para a pasta que receberá a pasta a ser copiada ou movida.</span><span class="sxs-lookup"><span data-stu-id="8de3a-118">[in] A pointer to the folder that is to receive the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="8de3a-119">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="8de3a-119">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="8de3a-120">no Um ponteiro para o nome da pasta copiada ou movida; caso contrário, NULL, que indica que a pasta copiada ou movida deverá ter o mesmo nome da pasta de origem (a pasta apontada por _lpEntryID_).</span><span class="sxs-lookup"><span data-stu-id="8de3a-120">[in] A pointer to the name of the copied or moved folder; otherwise, NULL, which indicates that the copied or moved folder should have the same name as the source folder (the folder pointed to by  _lpEntryID_).</span></span>
    
 <span data-ttu-id="8de3a-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8de3a-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="8de3a-122">no Uma alça da janela da caixa de diálogo indicador de progresso e janelas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8de3a-122">[in] A handle of the window for the progress indicator dialog box and related windows.</span></span> <span data-ttu-id="8de3a-123">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador FOLDER_DIALOG esteja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="8de3a-123">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="8de3a-124">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="8de3a-124">_lpProgress_</span></span>
  
> <span data-ttu-id="8de3a-125">no Um ponteiro para um objeto Progress que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="8de3a-125">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="8de3a-126">Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="8de3a-126">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="8de3a-127">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG esteja definido em _parâmetroulflags_.</span><span class="sxs-lookup"><span data-stu-id="8de3a-127">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="8de3a-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8de3a-128">_ulFlags_</span></span>
  
> <span data-ttu-id="8de3a-129">no Uma bitmask de sinalizadores que controlam como a operação de cópia ou movimentação é realizada.</span><span class="sxs-lookup"><span data-stu-id="8de3a-129">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="8de3a-130">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="8de3a-130">The following flags can be set:</span></span>
    
<span data-ttu-id="8de3a-131">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="8de3a-131">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="8de3a-132">Todas as subpastas da pasta devem ser copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="8de3a-132">All of the folder's subfolders should be copied or moved.</span></span> <span data-ttu-id="8de3a-133">Quando o COPY_SUBFOLDERS não está definido para uma operação de cópia, somente a pasta identificada por _lpEntryID_ é copiada.</span><span class="sxs-lookup"><span data-stu-id="8de3a-133">When COPY_SUBFOLDERS is not set for a copy operation, only the folder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="8de3a-134">Com uma operação de movimentação, o comportamento COPY_SUBFOLDERS é o padrão, independentemente de o sinalizador ser definido.</span><span class="sxs-lookup"><span data-stu-id="8de3a-134">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="8de3a-135">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="8de3a-135">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="8de3a-136">Solicita a exibição de um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="8de3a-136">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="8de3a-137">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="8de3a-137">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="8de3a-138">A pasta deve ser movida ao invés de ser copiada.</span><span class="sxs-lookup"><span data-stu-id="8de3a-138">The folder should be moved instead of copied.</span></span> <span data-ttu-id="8de3a-139">Se FOLDER_MOVE não for definido, a pasta será copiada.</span><span class="sxs-lookup"><span data-stu-id="8de3a-139">If FOLDER_MOVE is not set, the folder is copied.</span></span>
    
<span data-ttu-id="8de3a-140">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8de3a-140">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8de3a-141">O nome da pasta está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="8de3a-141">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="8de3a-142">Se o sinalizador MAPI_UNICODE não estiver definido, o nome da pasta estará no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="8de3a-142">If the MAPI_UNICODE flag is not set, the name of the folder is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8de3a-143">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8de3a-143">Return value</span></span>

<span data-ttu-id="8de3a-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="8de3a-144">S_OK</span></span> 
  
> <span data-ttu-id="8de3a-145">A pasta foi copiada ou movida com êxito.</span><span class="sxs-lookup"><span data-stu-id="8de3a-145">The folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="8de3a-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="8de3a-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="8de3a-147">O nome da pasta que está sendo movida ou copiada é o mesmo que o de uma subpasta na pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="8de3a-147">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="8de3a-148">O provedor de repositório de mensagens exige que os nomes das pastas sejam exclusivos.</span><span class="sxs-lookup"><span data-stu-id="8de3a-148">The message store provider requires that folder names be unique.</span></span> <span data-ttu-id="8de3a-149">A operação é interrompida sem conclusão.</span><span class="sxs-lookup"><span data-stu-id="8de3a-149">The operation stops without completing.</span></span>
    
<span data-ttu-id="8de3a-150">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="8de3a-150">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="8de3a-151">A chamada teve êxito, mas nem todas as entradas foram copiadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="8de3a-151">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="8de3a-152">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8de3a-152">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="8de3a-153">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="8de3a-153">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="8de3a-154">Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="8de3a-154">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8de3a-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="8de3a-155">Remarks</span></span>

<span data-ttu-id="8de3a-156">O método **IMAPISupport:: CopyFolder** é implementado para objetos de suporte do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="8de3a-156">The **IMAPISupport::CopyFolder** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="8de3a-157">Os provedores de repositório de mensagens podem chamar **IMAPISupport:: CopyFolder** em sua implementação de [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md) para copiar ou mover uma única pasta de uma pasta pai para outra.</span><span class="sxs-lookup"><span data-stu-id="8de3a-157">Message store providers can call **IMAPISupport::CopyFolder** in their implementation of [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) to copy or move a single folder from one parent folder to another.</span></span> 
  
 <span data-ttu-id="8de3a-158">**IMAPISupport:: CopyFolder** adiciona a pasta copiada ou movida como uma subpasta da pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="8de3a-158">**IMAPISupport::CopyFolder** adds the copied or moved folder as a subfolder of the destination folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8de3a-159">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="8de3a-159">Notes to callers</span></span>

 <span data-ttu-id="8de3a-160">**IMAPISupport:: CopyFolder** permite renomear e mover simultaneamente pastas e a cópia ou movimentação de subpastas da pasta afetada.</span><span class="sxs-lookup"><span data-stu-id="8de3a-160">**IMAPISupport::CopyFolder** allows simultaneous renaming and moving of folders and the copying or moving of subfolders of the affected folder.</span></span> <span data-ttu-id="8de3a-161">Para copiar ou mover todas as subpastas aninhadas na pasta copiada ou movida, passe o sinalizador COPY_SUBFOLDERS no _parâmetroulflags_.</span><span class="sxs-lookup"><span data-stu-id="8de3a-161">To copy or move all subfolders nested in the copied or moved folder, pass the COPY_SUBFOLDERS flag in  _ulFlags_.</span></span> 
  
<span data-ttu-id="8de3a-162">Espere os seguintes valores de retorno sob as seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="8de3a-162">Expect the following return values under the following conditions:</span></span>
  
|<span data-ttu-id="8de3a-163">**Condition**</span><span class="sxs-lookup"><span data-stu-id="8de3a-163">**Condition**</span></span>|<span data-ttu-id="8de3a-164">**Valor de retorno**</span><span class="sxs-lookup"><span data-stu-id="8de3a-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8de3a-165">**CopyFolder** copiou ou moveu com êxito a pasta e todas as suas subpastas, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="8de3a-165">**CopyFolder** successfully copied or moved the folder and all its subfolders, if applicable.</span></span>  <br/> |<span data-ttu-id="8de3a-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="8de3a-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="8de3a-167">O **CopyFolder** não pôde copiar ou mover com êxito todas as pastas.</span><span class="sxs-lookup"><span data-stu-id="8de3a-167">**CopyFolder** was unable to successfully copy or move all of the folders.</span></span>  <br/> |<span data-ttu-id="8de3a-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="8de3a-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="8de3a-169">**CopyFolder** não pôde ser concluída.</span><span class="sxs-lookup"><span data-stu-id="8de3a-169">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="8de3a-170">Qualquer valor de erro</span><span class="sxs-lookup"><span data-stu-id="8de3a-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="8de3a-171">Se **CopyFolder** retornar um valor de erro, não prossiga com a suposição de que nenhum trabalho foi realizado.</span><span class="sxs-lookup"><span data-stu-id="8de3a-171">If **CopyFolder** returns an error value, do not proceed on the assumption that no work was done.</span></span> <span data-ttu-id="8de3a-172">Uma ou mais pastas podem ter sido copiadas ou movidas antes do **CopyFolder** ter falhado.</span><span class="sxs-lookup"><span data-stu-id="8de3a-172">One or more folders could have been copied or moved before **CopyFolder** experienced the failure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8de3a-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="8de3a-173">See also</span></span>



[<span data-ttu-id="8de3a-174">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8de3a-174">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

