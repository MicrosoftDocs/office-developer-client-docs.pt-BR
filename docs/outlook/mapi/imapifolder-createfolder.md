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
ms.openlocfilehash: 606d780aa59e363c30ddc7a5b562db64d845ccb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436759"
---
# <a name="imapifoldercreatefolder"></a><span data-ttu-id="ecb68-103">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ecb68-103">IMAPIFolder::CreateFolder</span></span>

  
  
<span data-ttu-id="ecb68-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecb68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecb68-105">Cria uma nova subpasta.</span><span class="sxs-lookup"><span data-stu-id="ecb68-105">Creates a new subfolder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ecb68-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ecb68-106">Parameters</span></span>

 <span data-ttu-id="ecb68-107">_ulFolderType_</span><span class="sxs-lookup"><span data-stu-id="ecb68-107">_ulFolderType_</span></span>
  
> <span data-ttu-id="ecb68-108">[in] O tipo de pasta a ser criado.</span><span class="sxs-lookup"><span data-stu-id="ecb68-108">[in] The type of folder to create.</span></span> <span data-ttu-id="ecb68-109">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="ecb68-109">The following flags can be set:</span></span>
    
<span data-ttu-id="ecb68-110">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="ecb68-110">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="ecb68-111">Uma pasta genérica deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="ecb68-111">A generic folder should be created.</span></span>
    
<span data-ttu-id="ecb68-112">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="ecb68-112">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="ecb68-113">Uma pasta de resultados de pesquisa deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="ecb68-113">A search-results folder should be created.</span></span>
    
 <span data-ttu-id="ecb68-114">_lpszFolderName_</span><span class="sxs-lookup"><span data-stu-id="ecb68-114">_lpszFolderName_</span></span>
  
> <span data-ttu-id="ecb68-115">[in] Um ponteiro para uma cadeia de caracteres que contém o nome da nova pasta.</span><span class="sxs-lookup"><span data-stu-id="ecb68-115">[in] A pointer to a string that contains the name for the new folder.</span></span> <span data-ttu-id="ecb68-116">Esse nome é a base para a propriedade PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) da nova pasta.</span><span class="sxs-lookup"><span data-stu-id="ecb68-116">This name is the basis for the new folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="ecb68-117">_lpszFolderComment_</span><span class="sxs-lookup"><span data-stu-id="ecb68-117">_lpszFolderComment_</span></span>
  
> <span data-ttu-id="ecb68-118">[in] Um ponteiro para uma cadeia de caracteres que contém um comentário associado à nova pasta.</span><span class="sxs-lookup"><span data-stu-id="ecb68-118">[in] A pointer to a string that contains a comment associated with the new folder.</span></span> <span data-ttu-id="ecb68-119">Essa cadeia de caracteres se torna o valor da propriedade PR_COMMENT **(** [PidTagComment](pidtagcomment-canonical-property.md)) da nova pasta.</span><span class="sxs-lookup"><span data-stu-id="ecb68-119">This string becomes the value of the new folder's **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) property.</span></span> <span data-ttu-id="ecb68-120">Se NULL for passado, a pasta não terá comentários iniciais.</span><span class="sxs-lookup"><span data-stu-id="ecb68-120">If NULL is passed, the folder has no initial comment.</span></span>
    
 <span data-ttu-id="ecb68-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ecb68-121">_lpInterface_</span></span>
  
> <span data-ttu-id="ecb68-122">[in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar a nova pasta.</span><span class="sxs-lookup"><span data-stu-id="ecb68-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new folder.</span></span> <span data-ttu-id="ecb68-123">Passar NULL faz com que o provedor de armazenamento de mensagens retorne a interface de pasta padrão, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="ecb68-123">Passing NULL causes the message store provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="ecb68-124">Os clientes devem passar NULL.</span><span class="sxs-lookup"><span data-stu-id="ecb68-124">Clients must pass NULL.</span></span> <span data-ttu-id="ecb68-125">Outros chamadores podem definir o  _parâmetro lpInterface_ como IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="ecb68-125">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="ecb68-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ecb68-126">_ulFlags_</span></span>
  
> <span data-ttu-id="ecb68-127">[in] Uma máscara de bits de sinalizadores que controla como a pasta é criada.</span><span class="sxs-lookup"><span data-stu-id="ecb68-127">[in] A bitmask of flags that controls how the folder is created.</span></span> <span data-ttu-id="ecb68-128">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="ecb68-128">The following flags can be set:</span></span>
    
<span data-ttu-id="ecb68-129">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ecb68-129">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ecb68-130">Permite que **CreateFolder** retorne com êxito, possivelmente antes da nova pasta estar totalmente disponível para o cliente de chamada.</span><span class="sxs-lookup"><span data-stu-id="ecb68-130">Allows **CreateFolder** to return successfully, possibly before the new folder is fully available to the calling client.</span></span> <span data-ttu-id="ecb68-131">Se a nova pasta não estiver disponível, fazer uma chamada subsequente pode causar um erro.</span><span class="sxs-lookup"><span data-stu-id="ecb68-131">If the new folder is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="ecb68-132">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ecb68-132">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ecb68-133">O nome da pasta está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ecb68-133">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="ecb68-134">Se o MAPI_UNICODE não estiver definido, o nome da pasta está no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ecb68-134">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
<span data-ttu-id="ecb68-135">OPEN_IF_EXISTS</span><span class="sxs-lookup"><span data-stu-id="ecb68-135">OPEN_IF_EXISTS</span></span> 
  
> <span data-ttu-id="ecb68-136">Permite que o método tenha êxito mesmo se a pasta nomeada no parâmetro  _lpszFolderName_ já existir abrindo a pasta existente com esse nome.</span><span class="sxs-lookup"><span data-stu-id="ecb68-136">Allows the method to succeed even if the folder named in the  _lpszFolderName_ parameter already exists by opening the existing folder that has that name.</span></span> <span data-ttu-id="ecb68-137">Observe que os provedores de armazenamento de mensagens que permitem que pastas irmãos tenham o mesmo nome podem não abrir uma pasta existente se houver mais de um com o nome fornecido.</span><span class="sxs-lookup"><span data-stu-id="ecb68-137">Note that message store providers that allow sibling folders to have the same name might not open an existing folder if more than one exists with the supplied name.</span></span> 
    
 <span data-ttu-id="ecb68-138">_lppFolder_</span><span class="sxs-lookup"><span data-stu-id="ecb68-138">_lppFolder_</span></span>
  
> <span data-ttu-id="ecb68-139">[out] Um ponteiro para um ponteiro para a pasta recém-criada.</span><span class="sxs-lookup"><span data-stu-id="ecb68-139">[out] A pointer to a pointer to the newly created folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ecb68-140">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ecb68-140">Return value</span></span>

<span data-ttu-id="ecb68-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="ecb68-141">S_OK</span></span> 
  
> <span data-ttu-id="ecb68-142">A nova pasta foi criada ou aberta com êxito, se o sinalizador OPEN_IF_EXISTS estiver definido.</span><span class="sxs-lookup"><span data-stu-id="ecb68-142">The new folder has been successfully created or opened, if the OPEN_IF_EXISTS flag is set.</span></span>
    
<span data-ttu-id="ecb68-143">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ecb68-143">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ecb68-144">O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.</span><span class="sxs-lookup"><span data-stu-id="ecb68-144">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="ecb68-145">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="ecb68-145">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="ecb68-146">Já existe uma pasta com o nome dado _no parâmetro lpszFolderName._</span><span class="sxs-lookup"><span data-stu-id="ecb68-146">A folder that has the name given in the  _lpszFolderName_ parameter already exists.</span></span> <span data-ttu-id="ecb68-147">Os nomes das pastas devem ser exclusivos.</span><span class="sxs-lookup"><span data-stu-id="ecb68-147">Folder names must be unique.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ecb68-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecb68-148">Remarks</span></span>

<span data-ttu-id="ecb68-149">O **método IMAPIFolder::CreateFolder** cria uma subpasta na pasta atual e atribui um identificador de entrada à nova pasta.</span><span class="sxs-lookup"><span data-stu-id="ecb68-149">The **IMAPIFolder::CreateFolder** method creates a subfolder in the current folder and assigns an entry identifier to the new folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ecb68-150">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ecb68-150">Notes to callers</span></span>

<span data-ttu-id="ecb68-151">Quando **CreateFolder** retornar, esteja ciente de que o identificador de entrada para a nova pasta pode não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="ecb68-151">When **CreateFolder** returns, be aware that the entry identifier for the new folder might not be available.</span></span> <span data-ttu-id="ecb68-152">Alguns provedores de armazenamento de mensagens não disponibilizam identificadores de entrada até que você tenha chamado o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da nova pasta para salvá-la permanentemente.</span><span class="sxs-lookup"><span data-stu-id="ecb68-152">Some message store providers do not make entry identifiers available until after you have called the new folder's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to permanently save it.</span></span> <span data-ttu-id="ecb68-153">Isso é especialmente verdadeiro se você tiver definido o MAPI_DEFERRED_ERRORS sinalizador.</span><span class="sxs-lookup"><span data-stu-id="ecb68-153">This is especially true if you have set the MAPI_DEFERRED_ERRORS flag.</span></span> 
  
<span data-ttu-id="ecb68-154">Saiba que alguns provedores de armazenamento de mensagens sempre apontam o parâmetro _lppFolder_ para a interface padrão da pasta, independentemente do valor que você passa para o parâmetro _lpInterface._</span><span class="sxs-lookup"><span data-stu-id="ecb68-154">Be aware that some message store providers always point the  _lppFolder_ parameter to the folder's standard interface, regardless of the value that you pass in for the  _lpInterface_ parameter.</span></span> <span data-ttu-id="ecb68-155">Como o ponteiro da interface retornado pode não ser do tipo esperado, chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) da nova pasta para recuperar a propriedade **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ecb68-155">Because the interface pointer that is returned might not be of the type that you expect, call the new folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property.</span></span> <span data-ttu-id="ecb68-156">Se necessário, cast the pointer to a more appropriate type before you make other calls.</span><span class="sxs-lookup"><span data-stu-id="ecb68-156">If necessary, cast the pointer to a more appropriate type before you make other calls.</span></span>
  
<span data-ttu-id="ecb68-157">A maioria dos provedores de armazenamento de mensagens exige que o nome da nova pasta seja exclusivo em relação aos nomes de suas pastas irmãos.</span><span class="sxs-lookup"><span data-stu-id="ecb68-157">Most message store providers require the name of the new folder to be unique with respect to the names of its sibling folders.</span></span> <span data-ttu-id="ecb68-158">Ser capaz de manipular o MAPI_E_COLLISION de erro, que será retornado se essa regra não for seguida.</span><span class="sxs-lookup"><span data-stu-id="ecb68-158">Be able to handle the MAPI_E_COLLISION error value, which is returned if this rule is not followed.</span></span> 
  
<span data-ttu-id="ecb68-159">Para determinar o identificador de entrada da pasta recém-criada, chame o método **IMAPIProp::GetProps** da nova pasta para recuperar sua **propriedade PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ecb68-159">To determine the entry identifier of the newly created folder, call the new folder's **IMAPIProp::GetProps** method to retrieve its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ecb68-160">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ecb68-160">MFCMAPI reference</span></span>

<span data-ttu-id="ecb68-161">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ecb68-161">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ecb68-162">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ecb68-162">**File**</span></span>|<span data-ttu-id="ecb68-163">**Função**</span><span class="sxs-lookup"><span data-stu-id="ecb68-163">**Function**</span></span>|<span data-ttu-id="ecb68-164">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ecb68-164">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ecb68-165">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ecb68-165">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="ecb68-166">CMsgStoreDlg::OnCreateSubFolder</span><span class="sxs-lookup"><span data-stu-id="ecb68-166">CMsgStoreDlg::OnCreateSubFolder</span></span>  <br/> |<span data-ttu-id="ecb68-167">MFCMAPI usa o **método CMsgStoreDlg::OnCreateSubFolder** para criar novas pastas em MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="ecb68-167">MFCMAPI uses the **CMsgStoreDlg::OnCreateSubFolder** method to create new folders in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ecb68-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecb68-168">See also</span></span>



[<span data-ttu-id="ecb68-169">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="ecb68-169">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="ecb68-170">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ecb68-170">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="ecb68-171">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ecb68-171">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

