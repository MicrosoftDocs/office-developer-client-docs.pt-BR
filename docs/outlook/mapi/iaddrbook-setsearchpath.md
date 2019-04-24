---
title: IAddrBookSetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetSearchPath
api_type:
- COM
ms.assetid: fbff82de-77d3-411e-a30c-a37cefdd92fc
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8611249207811446ae47f056486ec498bf1e7eab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349305"
---
# <a name="iaddrbooksetsearchpath"></a><span data-ttu-id="53d91-103">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="53d91-103">IAddrBook::SetSearchPath</span></span>

  
  
<span data-ttu-id="53d91-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53d91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53d91-105">Define um novo caminho de pesquisa no perfil usado para o processo de resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="53d91-105">Sets a new search path in the profile that is used for the name resolution process.</span></span> 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="53d91-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53d91-106">Parameters</span></span>

 <span data-ttu-id="53d91-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53d91-107">_ulFlags_</span></span>
  
> <span data-ttu-id="53d91-108">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="53d91-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="53d91-109">_lpSearchPath_</span><span class="sxs-lookup"><span data-stu-id="53d91-109">_lpSearchPath_</span></span>
  
> <span data-ttu-id="53d91-110">no Um ponteiro para a estrutura [SRowSet](srowset.md) usada para manter o caminho de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="53d91-110">[in] A pointer to the [SRowSet](srowset.md) structure used to hold the search path.</span></span> <span data-ttu-id="53d91-111">A primeira propriedade para cada membro de **aRow** em **SRowSet** deve ser **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="53d91-111">The first property for each **aRow** member in **SRowSet** must be **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53d91-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="53d91-112">Return value</span></span>

<span data-ttu-id="53d91-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="53d91-113">S_OK</span></span> 
  
> <span data-ttu-id="53d91-114">O caminho de pesquisa foi definido com êxito.</span><span class="sxs-lookup"><span data-stu-id="53d91-114">The search path was successfully set.</span></span>
    
<span data-ttu-id="53d91-115">MAPI_E_MISSING_REQUIRED_COLUMN</span><span class="sxs-lookup"><span data-stu-id="53d91-115">MAPI_E_MISSING_REQUIRED_COLUMN</span></span> 
  
> <span data-ttu-id="53d91-116">Um dos contêineres descritos na estrutura **SRowSet** não inclui a propriedade **PR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="53d91-116">One of the containers described in the **SRowSet** structure did not include its **PR_ENTRYID** property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="53d91-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="53d91-117">Remarks</span></span>

<span data-ttu-id="53d91-118">Os clientes e os provedores de serviços chamam o método **SetSearchPath** para salvar as alterações feitas na ordem de pesquisa do contêiner usada para resolver nomes com o método [IAddrBook:: ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="53d91-118">Clients and service providers call the **SetSearchPath** method to save changes that were made to the container search order that is used to resolve names with the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="53d91-119">O caminho de pesquisa é salvo entre as instâncias de uma sessão.</span><span class="sxs-lookup"><span data-stu-id="53d91-119">The search path is saved between instances of a session.</span></span> 
  
<span data-ttu-id="53d91-120">Os clientes e provedores não precisam chamar o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) para tornar as alterações no caminho de pesquisa permanentes.</span><span class="sxs-lookup"><span data-stu-id="53d91-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the search path changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53d91-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="53d91-121">See also</span></span>



[<span data-ttu-id="53d91-122">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="53d91-122">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="53d91-123">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="53d91-123">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="53d91-124">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="53d91-124">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="53d91-125">Propriedade canônica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="53d91-125">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="53d91-126">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="53d91-126">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

