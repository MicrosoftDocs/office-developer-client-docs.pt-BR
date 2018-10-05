---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3ab01f189734ac30b4c027f4e5596c88031b5f99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392708"
---
# <a name="iaddrbooksetdefaultdir"></a><span data-ttu-id="17be9-103">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="17be9-103">IAddrBook::SetDefaultDir</span></span>

  
  
<span data-ttu-id="17be9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17be9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17be9-105">Estabelece o contêiner especificado como o contêiner de catálogo de endereços padrão.</span><span class="sxs-lookup"><span data-stu-id="17be9-105">Establishes the specified container as the default address book container.</span></span>
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="17be9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17be9-106">Parameters</span></span>

 <span data-ttu-id="17be9-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="17be9-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="17be9-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="17be9-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="17be9-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="17be9-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="17be9-110">[in] Um ponteiro para o identificador de entrada do contêiner de catálogo de endereços padrão.</span><span class="sxs-lookup"><span data-stu-id="17be9-110">[in] A pointer to the entry identifier of the default address book container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="17be9-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="17be9-111">Return value</span></span>

<span data-ttu-id="17be9-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="17be9-112">S_OK</span></span> 
  
> <span data-ttu-id="17be9-113">O contêiner de catálogo de endereços padrão foi definido com êxito.</span><span class="sxs-lookup"><span data-stu-id="17be9-113">The default address book container was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17be9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="17be9-114">Remarks</span></span>

<span data-ttu-id="17be9-115">Provedores de serviços e clientes chame o método de **SetDefaultDir** para estabelecer um novo contêiner de catálogo de endereços padrão.</span><span class="sxs-lookup"><span data-stu-id="17be9-115">Clients and service providers call the **SetDefaultDir** method to establish a new default address book container.</span></span> <span data-ttu-id="17be9-116">O contêiner padrão é o contêiner em que o usuário vê exibido no catálogo de endereços quando o catálogo de endereços é aberto pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="17be9-116">The default container is the container that the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="17be9-117">**SetDefaultDir** salva o contêiner padrão como uma entrada no perfil.</span><span class="sxs-lookup"><span data-stu-id="17be9-117">**SetDefaultDir** saves the default container as an entry in the profile.</span></span> <span data-ttu-id="17be9-118">O contêiner permanece como padrão até que outra chamada para **SetDefaultDir** é feita na mesma sessão ou em outra sessão, ou o contêiner é removido.</span><span class="sxs-lookup"><span data-stu-id="17be9-118">The container remains as the default until either another call to **SetDefaultDir** is made in the same session or in another session, or the container is removed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="17be9-119">A propriedade [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) corresponde à configuração da **Escolha automaticamente** na caixa de diálogo Opções do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="17be9-119">The [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="17be9-120">Quando essa propriedade existe na seção de perfil [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) e estiver definida como **true**, a caixa de diálogo Catálogo de endereços não são mais padrões para o contêiner especificado por **SetDefaultDir**, mas escolhe um catálogo de endereços que considera do Microsoft Outlook apropriada para o contexto no qual a caixa de diálogo foi exibida.</span><span class="sxs-lookup"><span data-stu-id="17be9-120">When this property exists in the [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by **SetDefaultDir**, but chooses an address book that Microsoft Outlook considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="17be9-121">Observe que isso pode resultar em uma experiência ruim para provedores de catálogo de endereços de terceiros.</span><span class="sxs-lookup"><span data-stu-id="17be9-121">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="17be9-122">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="17be9-122">MFCMAPI reference</span></span>

<span data-ttu-id="17be9-123">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="17be9-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="17be9-124">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="17be9-124">**File**</span></span>|<span data-ttu-id="17be9-125">**Função**</span><span class="sxs-lookup"><span data-stu-id="17be9-125">**Function**</span></span>|<span data-ttu-id="17be9-126">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="17be9-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="17be9-127">Abcontdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="17be9-127">Abcontdlg.cpp</span></span>  <br/> |<span data-ttu-id="17be9-128">CAbContDlg::OnSetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="17be9-128">CAbContDlg::OnSetDefaultDir</span></span>  <br/> |<span data-ttu-id="17be9-129">MFCMAPI usa o método **SetDefaultDir** para tornar o contêiner de catálogo de endereços especificado o padrão de um.</span><span class="sxs-lookup"><span data-stu-id="17be9-129">MFCMAPI uses the **SetDefaultDir** method to make the specified address book container the default one.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17be9-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="17be9-130">See also</span></span>



[<span data-ttu-id="17be9-131">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="17be9-131">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="17be9-132">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="17be9-132">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="17be9-133">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="17be9-133">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="17be9-134">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="17be9-134">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="17be9-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="17be9-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="17be9-136">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="17be9-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

