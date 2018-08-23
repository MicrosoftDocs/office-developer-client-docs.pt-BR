---
title: IMAPIFolderCreateFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 694f7ec5715a7348c9bd90c28d14f30d43d19974
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581780"
---
# <a name="imapifoldercreatefolder"></a><span data-ttu-id="403cf-103">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="403cf-103">IMAPIFolder::CreateFolder</span></span>

  
  
<span data-ttu-id="403cf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="403cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="403cf-105">Cria uma nova subpasta.</span><span class="sxs-lookup"><span data-stu-id="403cf-105">Creates a new subfolder.</span></span>
  
```cpp
HRESULT CreateFolder(
  ULONG ulFolderType,
  LPSTR lpszFolderName,
  LPSTR lpszFolderComment,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMAPIFOLDER FAR * lppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="403cf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="403cf-106">Parameters</span></span>

 <span data-ttu-id="403cf-107">_ulFolderType_</span><span class="sxs-lookup"><span data-stu-id="403cf-107">_ulFolderType_</span></span>
  
> <span data-ttu-id="403cf-108">[in] O tipo da pasta a ser criada.</span><span class="sxs-lookup"><span data-stu-id="403cf-108">[in] The type of folder to create.</span></span> <span data-ttu-id="403cf-109">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="403cf-109">The following flags can be set:</span></span>
    
<span data-ttu-id="403cf-110">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="403cf-110">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="403cf-111">Uma pasta genérica deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="403cf-111">A generic folder should be created.</span></span>
    
<span data-ttu-id="403cf-112">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="403cf-112">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="403cf-113">Uma pasta de resultados de pesquisa deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="403cf-113">A search-results folder should be created.</span></span>
    
 <span data-ttu-id="403cf-114">_lpszFolderName_</span><span class="sxs-lookup"><span data-stu-id="403cf-114">_lpszFolderName_</span></span>
  
> <span data-ttu-id="403cf-115">[in] Um ponteiro para uma cadeia de caracteres que contém o nome da nova pasta.</span><span class="sxs-lookup"><span data-stu-id="403cf-115">[in] A pointer to a string that contains the name for the new folder.</span></span> <span data-ttu-id="403cf-116">Esse nome é a base para a propriedade de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) da nova pasta.</span><span class="sxs-lookup"><span data-stu-id="403cf-116">This name is the basis for the new folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="403cf-117">_lpszFolderComment_</span><span class="sxs-lookup"><span data-stu-id="403cf-117">_lpszFolderComment_</span></span>
  
> <span data-ttu-id="403cf-118">[in] Um ponteiro para uma cadeia de caracteres que contém um comentário associado a nova pasta.</span><span class="sxs-lookup"><span data-stu-id="403cf-118">[in] A pointer to a string that contains a comment associated with the new folder.</span></span> <span data-ttu-id="403cf-119">Esta cadeia de caracteres torna-se o valor da propriedade de **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) da nova pasta.</span><span class="sxs-lookup"><span data-stu-id="403cf-119">This string becomes the value of the new folder's **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) property.</span></span> <span data-ttu-id="403cf-120">Se NULL for passado, a pasta não tem nenhum comentário inicial.</span><span class="sxs-lookup"><span data-stu-id="403cf-120">If NULL is passed, the folder has no initial comment.</span></span>
    
 <span data-ttu-id="403cf-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="403cf-121">_lpInterface_</span></span>
  
> <span data-ttu-id="403cf-122">[in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar a nova pasta.</span><span class="sxs-lookup"><span data-stu-id="403cf-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new folder.</span></span> <span data-ttu-id="403cf-123">Passar NULL faz com que o provedor de armazenamento de mensagem retornar a interface de pasta padrão, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="403cf-123">Passing NULL causes the message store provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="403cf-124">Os clientes devem passar NULL.</span><span class="sxs-lookup"><span data-stu-id="403cf-124">Clients must pass NULL.</span></span> <span data-ttu-id="403cf-125">Outros chamadores podem definir o parâmetro _lpInterface_ IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="403cf-125">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="403cf-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="403cf-126">_ulFlags_</span></span>
  
> <span data-ttu-id="403cf-127">[in] Uma bitmask dos sinalizadores que controla como a pasta é criada.</span><span class="sxs-lookup"><span data-stu-id="403cf-127">[in] A bitmask of flags that controls how the folder is created.</span></span> <span data-ttu-id="403cf-128">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="403cf-128">The following flags can be set:</span></span>
    
<span data-ttu-id="403cf-129">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="403cf-129">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="403cf-130">Permite **CreateFolder** retornar com êxito, possivelmente antes que a nova pasta esteja totalmente disponível para o cliente da chamada.</span><span class="sxs-lookup"><span data-stu-id="403cf-130">Allows **CreateFolder** to return successfully, possibly before the new folder is fully available to the calling client.</span></span> <span data-ttu-id="403cf-131">Se a nova pasta não estiver disponível, fazendo uma chamada subsequente a ele pode causar um erro.</span><span class="sxs-lookup"><span data-stu-id="403cf-131">If the new folder is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="403cf-132">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="403cf-132">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="403cf-133">O nome da pasta é no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="403cf-133">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="403cf-134">Se o sinalizador MAPI_UNICODE não estiver definido, o nome da pasta é no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="403cf-134">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
<span data-ttu-id="403cf-135">OPEN_IF_EXISTS</span><span class="sxs-lookup"><span data-stu-id="403cf-135">OPEN_IF_EXISTS</span></span> 
  
> <span data-ttu-id="403cf-136">Permite que o método seja bem-sucedido, mesmo se a pasta chamada no parâmetro _lpszFolderName_ já existe abrindo a pasta existente que recebeu esse nome.</span><span class="sxs-lookup"><span data-stu-id="403cf-136">Allows the method to succeed even if the folder named in the  _lpszFolderName_ parameter already exists by opening the existing folder that has that name.</span></span> <span data-ttu-id="403cf-137">Observe que os provedores de armazenamento de mensagem que permitem irmão pastas para ter o mesmo nome não podem abrir uma pasta existente se mais de um existir com o nome fornecido.</span><span class="sxs-lookup"><span data-stu-id="403cf-137">Note that message store providers that allow sibling folders to have the same name might not open an existing folder if more than one exists with the supplied name.</span></span> 
    
 <span data-ttu-id="403cf-138">_lppFolder_</span><span class="sxs-lookup"><span data-stu-id="403cf-138">_lppFolder_</span></span>
  
> <span data-ttu-id="403cf-139">[out] Um ponteiro para um ponteiro para a pasta recém-criada.</span><span class="sxs-lookup"><span data-stu-id="403cf-139">[out] A pointer to a pointer to the newly created folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="403cf-140">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="403cf-140">Return value</span></span>

<span data-ttu-id="403cf-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="403cf-141">S_OK</span></span> 
  
> <span data-ttu-id="403cf-142">A nova pasta foi criada ou aberta, se o sinalizador OPEN_IF_EXISTS for definido com êxito.</span><span class="sxs-lookup"><span data-stu-id="403cf-142">The new folder has been successfully created or opened, if the OPEN_IF_EXISTS flag is set.</span></span>
    
<span data-ttu-id="403cf-143">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="403cf-143">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="403cf-144">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="403cf-144">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="403cf-145">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="403cf-145">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="403cf-146">Uma pasta que tem o nome fornecido no parâmetro _lpszFolderName_ já existe.</span><span class="sxs-lookup"><span data-stu-id="403cf-146">A folder that has the name given in the  _lpszFolderName_ parameter already exists.</span></span> <span data-ttu-id="403cf-147">Nomes de pasta devem ser exclusivos.</span><span class="sxs-lookup"><span data-stu-id="403cf-147">Folder names must be unique.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="403cf-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="403cf-148">Remarks</span></span>

<span data-ttu-id="403cf-149">O método **IMAPIFolder::CreateFolder** cria uma subpasta na pasta atual e atribui um identificador de entrada para a nova pasta.</span><span class="sxs-lookup"><span data-stu-id="403cf-149">The **IMAPIFolder::CreateFolder** method creates a subfolder in the current folder and assigns an entry identifier to the new folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="403cf-150">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="403cf-150">Notes to callers</span></span>

<span data-ttu-id="403cf-151">Quando **CreateFolder** retorna, lembre-se de que o identificador de entrada para a nova pasta pode não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="403cf-151">When **CreateFolder** returns, be aware that the entry identifier for the new folder might not be available.</span></span> <span data-ttu-id="403cf-152">Alguns provedores de armazenamento de mensagem não disponibilizar identificadores de entrada até depois de ter chamado o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da nova pasta para permanentemente salvá-la.</span><span class="sxs-lookup"><span data-stu-id="403cf-152">Some message store providers do not make entry identifiers available until after you have called the new folder's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to permanently save it.</span></span> <span data-ttu-id="403cf-153">Isso acontece principalmente se você tiver configurado o sinalizador MAPI_DEFERRED_ERRORS.</span><span class="sxs-lookup"><span data-stu-id="403cf-153">This is especially true if you have set the MAPI_DEFERRED_ERRORS flag.</span></span> 
  
<span data-ttu-id="403cf-154">Lembre-se de que alguns provedores de armazenamento de mensagem sempre apontam o parâmetro _lppFolder_ para interface de padrão da pasta, independentemente do valor que você passa para o parâmetro _lpInterface_ .</span><span class="sxs-lookup"><span data-stu-id="403cf-154">Be aware that some message store providers always point the  _lppFolder_ parameter to the folder's standard interface, regardless of the value that you pass in for the  _lpInterface_ parameter.</span></span> <span data-ttu-id="403cf-155">Porque o ponteiro de interface retornada pode não ser do tipo que você espera, chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) da nova pasta para recuperar a propriedade **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="403cf-155">Because the interface pointer that is returned might not be of the type that you expect, call the new folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property.</span></span> <span data-ttu-id="403cf-156">Se necessário, converta o ponteiro para um tipo mais apropriado antes de fazer outras chamadas.</span><span class="sxs-lookup"><span data-stu-id="403cf-156">If necessary, cast the pointer to a more appropriate type before you make other calls.</span></span>
  
<span data-ttu-id="403cf-157">A maioria dos provedores de armazenamento de mensagem exigem o nome da nova pasta seja exclusivo com relação aos nomes das suas pastas irmão.</span><span class="sxs-lookup"><span data-stu-id="403cf-157">Most message store providers require the name of the new folder to be unique with respect to the names of its sibling folders.</span></span> <span data-ttu-id="403cf-158">Ser capaz de manipular o valor de erro do MAPI_E_COLLISION, será retornado se esta regra não é seguida.</span><span class="sxs-lookup"><span data-stu-id="403cf-158">Be able to handle the MAPI_E_COLLISION error value, which is returned if this rule is not followed.</span></span> 
  
<span data-ttu-id="403cf-159">Para determinar o identificador de entrada da pasta recém-criada, chame o método de **IMAPIProp::GetProps** da nova pasta para recuperar sua propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="403cf-159">To determine the entry identifier of the newly created folder, call the new folder's **IMAPIProp::GetProps** method to retrieve its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="403cf-160">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="403cf-160">MFCMAPI reference</span></span>

<span data-ttu-id="403cf-161">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="403cf-161">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="403cf-162">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="403cf-162">**File**</span></span>|<span data-ttu-id="403cf-163">**Function**</span><span class="sxs-lookup"><span data-stu-id="403cf-163">**Function**</span></span>|<span data-ttu-id="403cf-164">**Comment**</span><span class="sxs-lookup"><span data-stu-id="403cf-164">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="403cf-165">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="403cf-165">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="403cf-166">CMsgStoreDlg::OnCreateSubFolder</span><span class="sxs-lookup"><span data-stu-id="403cf-166">CMsgStoreDlg::OnCreateSubFolder</span></span>  <br/> |<span data-ttu-id="403cf-167">MFCMAPI usa o método **CMsgStoreDlg::OnCreateSubFolder** para criar novas pastas no MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="403cf-167">MFCMAPI uses the **CMsgStoreDlg::OnCreateSubFolder** method to create new folders in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="403cf-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="403cf-168">See also</span></span>



[<span data-ttu-id="403cf-169">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="403cf-169">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="403cf-170">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="403cf-170">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="403cf-171">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="403cf-171">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

