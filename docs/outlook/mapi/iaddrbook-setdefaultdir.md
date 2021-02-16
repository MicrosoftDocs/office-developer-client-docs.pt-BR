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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341696"
---
# <a name="iaddrbooksetdefaultdir"></a><span data-ttu-id="e3389-103">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="e3389-103">IAddrBook::SetDefaultDir</span></span>

  
  
<span data-ttu-id="e3389-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3389-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3389-105">Estabelece o contêiner especificado como o contêiner de agendamento padrão.</span><span class="sxs-lookup"><span data-stu-id="e3389-105">Establishes the specified container as the default address book container.</span></span>
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="e3389-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3389-106">Parameters</span></span>

 <span data-ttu-id="e3389-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e3389-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="e3389-108">[in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="e3389-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e3389-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e3389-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="e3389-110">[in] Um ponteiro para o identificador de entrada do contêiner de agendamento padrão.</span><span class="sxs-lookup"><span data-stu-id="e3389-110">[in] A pointer to the entry identifier of the default address book container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e3389-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e3389-111">Return value</span></span>

<span data-ttu-id="e3389-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3389-112">S_OK</span></span> 
  
> <span data-ttu-id="e3389-113">O contêiner padrão do livro de endereços foi definido com êxito.</span><span class="sxs-lookup"><span data-stu-id="e3389-113">The default address book container was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3389-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3389-114">Remarks</span></span>

<span data-ttu-id="e3389-115">Os clientes e provedores de serviços chamam **o método SetDefaultDir** para estabelecer um novo contêiner de agendamento de endereços padrão.</span><span class="sxs-lookup"><span data-stu-id="e3389-115">Clients and service providers call the **SetDefaultDir** method to establish a new default address book container.</span></span> <span data-ttu-id="e3389-116">O contêiner padrão é o contêiner que o usuário vê exibido no livro de endereços quando o livro de endereços é aberto pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="e3389-116">The default container is the container that the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="e3389-117">**SetDefaultDir** salva o contêiner padrão como uma entrada no perfil.</span><span class="sxs-lookup"><span data-stu-id="e3389-117">**SetDefaultDir** saves the default container as an entry in the profile.</span></span> <span data-ttu-id="e3389-118">O contêiner permanece como padrão até que outra chamada para **SetDefaultDir** seja feita na mesma sessão ou em outra sessão, ou o contêiner seja removido.</span><span class="sxs-lookup"><span data-stu-id="e3389-118">The container remains as the default until either another call to **SetDefaultDir** is made in the same session or in another session, or the container is removed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e3389-119">A [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) propriedade corresponde à configuração Escolher **automaticamente** na caixa de diálogo Opções do Address Book.</span><span class="sxs-lookup"><span data-stu-id="e3389-119">The [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="e3389-120">Quando essa propriedade existe na seção de perfil [do IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) e está definida como **true**, a caixa de diálogo do Address Book não assume mais o contêiner especificado por **SetDefaultDir**, mas escolhe um livro de endereços que o Microsoft Outlook considera apropriado para o contexto no qual a caixa de diálogo foi exibida.</span><span class="sxs-lookup"><span data-stu-id="e3389-120">When this property exists in the [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by **SetDefaultDir**, but chooses an address book that Microsoft Outlook considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="e3389-121">Observe que isso pode resultar em uma experiência ruim para provedores de agendas de terceiros.</span><span class="sxs-lookup"><span data-stu-id="e3389-121">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e3389-122">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e3389-122">MFCMAPI reference</span></span>

<span data-ttu-id="e3389-123">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e3389-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e3389-124">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="e3389-124">**File**</span></span>|<span data-ttu-id="e3389-125">**Função**</span><span class="sxs-lookup"><span data-stu-id="e3389-125">**Function**</span></span>|<span data-ttu-id="e3389-126">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="e3389-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e3389-127">Abcontdlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e3389-127">Abcontdlg.cpp</span></span>  <br/> |<span data-ttu-id="e3389-128">CAbContDlg::OnSetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="e3389-128">CAbContDlg::OnSetDefaultDir</span></span>  <br/> |<span data-ttu-id="e3389-129">MFCMAPI usa o **método SetDefaultDir** para tornar o contêiner do livro de endereços especificado o padrão.</span><span class="sxs-lookup"><span data-stu-id="e3389-129">MFCMAPI uses the **SetDefaultDir** method to make the specified address book container the default one.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3389-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3389-130">See also</span></span>



[<span data-ttu-id="e3389-131">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="e3389-131">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="e3389-132">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="e3389-132">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="e3389-133">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="e3389-133">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="e3389-134">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="e3389-134">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="e3389-135">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e3389-135">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="e3389-136">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e3389-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

