---
title: IAddrBookGetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetDefaultDir
api_type:
- COM
ms.assetid: 7a9fdf3f-fd76-40fb-8217-967c6efba5f6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d9ad74d8ae02a49ee3c222394caedfd571f84b1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436871"
---
# <a name="iaddrbookgetdefaultdir"></a><span data-ttu-id="74448-103">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="74448-103">IAddrBook::GetDefaultDir</span></span>

  
  
<span data-ttu-id="74448-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74448-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74448-105">Retorna o identificador de entrada para o contêiner do catálogo de endereços inicial.</span><span class="sxs-lookup"><span data-stu-id="74448-105">Returns the entry identifier for the initial address book container.</span></span>
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="74448-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74448-106">Parameters</span></span>

 <span data-ttu-id="74448-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="74448-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="74448-108">bota Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="74448-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="74448-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="74448-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="74448-110">bota Um ponteiro para um ponteiro para o identificador de entrada do contêiner padrão.</span><span class="sxs-lookup"><span data-stu-id="74448-110">[out] A pointer to a pointer to the entry identifier of the default container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="74448-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="74448-111">Return value</span></span>

<span data-ttu-id="74448-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="74448-112">S_OK</span></span> 
  
> <span data-ttu-id="74448-113">O identificador de entrada do contêiner padrão foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="74448-113">The entry identifier of the default container was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="74448-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="74448-114">Remarks</span></span>

<span data-ttu-id="74448-115">Aplicativos cliente e provedores de serviços chamam o método **GetDefaultDir** para recuperar o identificador de entrada do contêiner de catálogo de endereços padrão.</span><span class="sxs-lookup"><span data-stu-id="74448-115">Client applications and service providers call the **GetDefaultDir** method to retrieve the entry identifier of the default address book container.</span></span> <span data-ttu-id="74448-116">O contêiner padrão é o que o usuário vê exibido no catálogo de endereços quando o catálogo de endereços é aberto pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="74448-116">The default container is what the user sees displayed in the address book when the address book is first opened.</span></span> <span data-ttu-id="74448-117">Se um contêiner padrão não tiver sido definido por uma chamada para o método [IAddrBook:: SetDefaultDir](iaddrbook-setdefaultdir.md) , MAPI atribui como o contêiner padrão o primeiro contêiner com nomes que não sejam o catálogo de endereços pessoal (PAB).</span><span class="sxs-lookup"><span data-stu-id="74448-117">If a default container has not been set by a call to the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method, MAPI assigns as the default container the first container with names that is not the personal address book (PAB).</span></span> <span data-ttu-id="74448-118">Se esse contêiner não puder ser localizado, o PAB se tornará o contêiner padrão.</span><span class="sxs-lookup"><span data-stu-id="74448-118">If such a container cannot be found, the PAB becomes the default container.</span></span> 
  
<span data-ttu-id="74448-119">Para definir o diretório padrão, um cliente ou provedor chama o método **SetDefaultDir** .</span><span class="sxs-lookup"><span data-stu-id="74448-119">To set the default directory, a client or provider calls the **SetDefaultDir** method.</span></span> <span data-ttu-id="74448-120">Os clientes e provedores não precisam chamar o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) ; como as alterações no catálogo de endereços não são transacionadas, as alterações são imediatamente feitas permanentes.</span><span class="sxs-lookup"><span data-stu-id="74448-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method; because changes to the address book are not transacted, changes are immediately made permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="74448-121">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="74448-121">MFCMAPI reference</span></span>

<span data-ttu-id="74448-122">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="74448-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="74448-123">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="74448-123">**File**</span></span>|<span data-ttu-id="74448-124">**Função**</span><span class="sxs-lookup"><span data-stu-id="74448-124">**Function**</span></span>|<span data-ttu-id="74448-125">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="74448-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="74448-126">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="74448-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="74448-127">CMainDlg:: OnOpenDefaultDir</span><span class="sxs-lookup"><span data-stu-id="74448-127">CMainDlg::OnOpenDefaultDir</span></span>  <br/> |<span data-ttu-id="74448-128">MFCMAPI usa o método **GetDefaultDir** para obter a ID do contêiner de catálogo de endereços padrão.</span><span class="sxs-lookup"><span data-stu-id="74448-128">MFCMAPI uses the **GetDefaultDir** method to get the ID for the default address book container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="74448-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="74448-129">See also</span></span>



[<span data-ttu-id="74448-130">IAddrBook::SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="74448-130">IAddrBook::SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md)
  
[<span data-ttu-id="74448-131">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="74448-131">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="74448-132">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="74448-132">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="74448-133">Propriedade canônica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="74448-133">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="74448-134">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="74448-134">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="74448-135">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="74448-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

