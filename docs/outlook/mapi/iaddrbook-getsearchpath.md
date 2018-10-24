---
title: IAddrBookGetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetSearchPath
api_type:
- COM
ms.assetid: 43b51a66-71fa-4e10-93e4-d533b48af4de
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7bf69e560142ab282d6545389e02766389e4d018
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580695"
---
# <a name="iaddrbookgetsearchpath"></a><span data-ttu-id="974f3-103">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="974f3-103">IAddrBook::GetSearchPath</span></span>

  
  
<span data-ttu-id="974f3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="974f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="974f3-105">Retorna uma lista ordenada de identificadores de entrada dos contêineres a serem incluídos no processo de resolução de nome iniciado pelo método [IAddrBook::ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="974f3-105">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="974f3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="974f3-106">Parameters</span></span>

 <span data-ttu-id="974f3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="974f3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="974f3-108">[in] Uma bitmask dos sinalizadores que controla o tipo das cadeias de caracteres retornada no caminho de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="974f3-108">[in] A bitmask of flags that controls the type of the strings returned in the search path.</span></span> <span data-ttu-id="974f3-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="974f3-109">The following flag can be set:</span></span>
    
<span data-ttu-id="974f3-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="974f3-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="974f3-111">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="974f3-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="974f3-112">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="974f3-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="974f3-113">_lppSearchPath_</span><span class="sxs-lookup"><span data-stu-id="974f3-113">_lppSearchPath_</span></span>
  
> <span data-ttu-id="974f3-114">[out] Um ponteiro para um ponteiro para uma lista ordenada de identificadores de entrada do contêiner.</span><span class="sxs-lookup"><span data-stu-id="974f3-114">[out] A pointer to a pointer to an ordered list of container entry identifiers.</span></span> <span data-ttu-id="974f3-115">**GetSearchPath** armazena a lista ordenada em uma estrutura [SRowSet](srowset.md) .</span><span class="sxs-lookup"><span data-stu-id="974f3-115">**GetSearchPath** stores the ordered list in an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="974f3-116">Se não houver nenhuma contêineres na hierarquia de catálogo de endereços, será retornado zero na estrutura **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="974f3-116">If there are no containers in the address book hierarchy, zero is returned in the **SRowSet** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="974f3-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="974f3-117">Return value</span></span>

<span data-ttu-id="974f3-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="974f3-118">S_OK</span></span> 
  
> <span data-ttu-id="974f3-119">O caminho de pesquisa foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="974f3-119">The search path was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="974f3-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="974f3-120">Remarks</span></span>

<span data-ttu-id="974f3-121">Provedores de serviços e clientes chame o método de **GetSearchPath** para obter o caminho de pesquisa que é usado para resolver nomes com o método **ResolveName** .</span><span class="sxs-lookup"><span data-stu-id="974f3-121">Clients and service providers call the **GetSearchPath** method to get the search path that is used to resolve names with the **ResolveName** method.</span></span> <span data-ttu-id="974f3-122">Normalmente, os clientes chame o método de [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) para estabelecer um caminho de pesquisa do contêiner no perfil antes de que ligarem **GetSearchPath** para recuperá-la.</span><span class="sxs-lookup"><span data-stu-id="974f3-122">Typically, clients call the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method to establish a container search path in the profile before they call **GetSearchPath** to retrieve it.</span></span> <span data-ttu-id="974f3-123">No entanto, chamar **SetSearchPath** é opcional.</span><span class="sxs-lookup"><span data-stu-id="974f3-123">However, calling **SetSearchPath** is optional.</span></span> 
  
<span data-ttu-id="974f3-124">Se **SetSearchPath** nunca tiver sido chamado, o **GetSearchPath** cria um caminho ao trabalho por meio do endereço tabelas de hierarquias do livro.</span><span class="sxs-lookup"><span data-stu-id="974f3-124">If **SetSearchPath** has never been called, **GetSearchPath** builds a path by working through the address book's hierarchy tables.</span></span> <span data-ttu-id="974f3-125">O caminho de pesquisa padrão estabelecido pelo **GetSearchPath** consiste nos seguintes contêineres na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="974f3-125">The default search path established by **GetSearchPath** consists of the following containers in the following order:</span></span> 
  
1. <span data-ttu-id="974f3-126">O primeiro recipiente com permissão de leitura/gravação, normalmente o catálogo de endereços pessoal (PAB).</span><span class="sxs-lookup"><span data-stu-id="974f3-126">The first container with read/write permission, usually the personal address book (PAB).</span></span>
    
2. <span data-ttu-id="974f3-127">Cada contêiner que tem sua propriedade **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) definida como DT_GLOBAL.</span><span class="sxs-lookup"><span data-stu-id="974f3-127">Every container that has its **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) property set to DT_GLOBAL.</span></span> <span data-ttu-id="974f3-128">Essa configuração indica que o contêiner retém os destinatários.</span><span class="sxs-lookup"><span data-stu-id="974f3-128">This setting indicates that the container holds recipients.</span></span> 
    
3. <span data-ttu-id="974f3-129">O contêiner designado como padrão, se não houver nenhuma contêineres que têm o sinalizador DT_GLOBAL definido em sua propriedade **PR_DISPLAY_TYPE** e o contêiner padrão difere do contêiner primeiro com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="974f3-129">The container designated as the default, if there are no containers that have the DT_GLOBAL flag set in their **PR_DISPLAY_TYPE** property and the default container differs from the first container with read/write permission.</span></span> 
    
<span data-ttu-id="974f3-130">Se tiver sido chamado **SetSearchPath** , **GetSearchPath** constrói um caminho usando os contêineres do catálogo de endereços que tiverem sido armazenados no perfil.</span><span class="sxs-lookup"><span data-stu-id="974f3-130">If **SetSearchPath** has been called, **GetSearchPath** builds a path by using the address book containers that have been stored in the profile.</span></span> <span data-ttu-id="974f3-131">**GetSearchPath** valida esse caminho antes de ele os retorna ao chamador.</span><span class="sxs-lookup"><span data-stu-id="974f3-131">**GetSearchPath** validates this path before it returns it to the caller.</span></span> 
  
<span data-ttu-id="974f3-132">Após a primeira chamada para **SetSearchPath**, as chamadas subsequentes **SetSearchPath** devem ser usadas para modificar o caminho de pesquisa retornado por **GetSearchPath**.</span><span class="sxs-lookup"><span data-stu-id="974f3-132">After the first call to **SetSearchPath**, subsequent calls to **SetSearchPath** must be used to modify the search path returned by **GetSearchPath**.</span></span> <span data-ttu-id="974f3-133">Em outras palavras, o cliente de chamada ou o provedor não recebe o caminho de pesquisa padrão após a primeira chamada para **SetSearchPath**.</span><span class="sxs-lookup"><span data-stu-id="974f3-133">In other words, the calling client or provider does not receive the default search path after the first call to **SetSearchPath**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="974f3-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="974f3-134">See also</span></span>



[<span data-ttu-id="974f3-135">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="974f3-135">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
  
[<span data-ttu-id="974f3-136">SRowSet</span><span class="sxs-lookup"><span data-stu-id="974f3-136">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="974f3-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="974f3-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

