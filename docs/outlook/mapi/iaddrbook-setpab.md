---
title: IAddrBookSetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 461b59ff4f4c8a93f3a9945b05e31aef9a2997bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569299"
---
# <a name="iaddrbooksetpab"></a><span data-ttu-id="77781-103">IAddrBook::SetPAB</span><span class="sxs-lookup"><span data-stu-id="77781-103">IAddrBook::SetPAB</span></span>

  
  
<span data-ttu-id="77781-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77781-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77781-105">Designa um contêiner específico como o catálogo de endereços pessoal (PAB).</span><span class="sxs-lookup"><span data-stu-id="77781-105">Designates a particular container as the personal address book (PAB).</span></span>
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="77781-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77781-106">Parameters</span></span>

 <span data-ttu-id="77781-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="77781-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="77781-108">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="77781-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="77781-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="77781-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="77781-110">[in] Um ponteiro para o identificador de entrada do contêiner que será designado como o PAB.</span><span class="sxs-lookup"><span data-stu-id="77781-110">[in] A pointer to the entry identifier of the container to be designated as the PAB.</span></span> <span data-ttu-id="77781-111">O parâmetro _lpEntryID_ não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="77781-111">The  _lpEntryID_ parameter cannot be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="77781-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="77781-112">Return value</span></span>

<span data-ttu-id="77781-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="77781-113">S_OK</span></span> 
  
> <span data-ttu-id="77781-114">O contêiner especificado como o PAB foi estabelecido.</span><span class="sxs-lookup"><span data-stu-id="77781-114">The specified container has been established as the PAB.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77781-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="77781-115">Remarks</span></span>

<span data-ttu-id="77781-116">Clientes e provedores de serviços de chamar o método de **SetPAB** para designar um contêiner específico como o PAB.</span><span class="sxs-lookup"><span data-stu-id="77781-116">Clients and service providers call the **SetPAB** method to designate a particular container as the PAB.</span></span> <span data-ttu-id="77781-117">O PAB é um contêiner que consiste de entradas copiadas de outros contêineres, bem como novas entradas.</span><span class="sxs-lookup"><span data-stu-id="77781-117">The PAB is a container that consists of entries copied from other containers as well as new entries.</span></span> 
  
<span data-ttu-id="77781-118">Uma chamada para **SetPAB** estabelece um contêiner como o PAB até contêiner em questão se tornar indisponível ou um novo contêiner se torna o PAB por meio de uma chamada subsequente **SetPAB**.</span><span class="sxs-lookup"><span data-stu-id="77781-118">A call to **SetPAB** establishes a container as the PAB until that container is made unavailable or a new container becomes the PAB through a subsequent call to **SetPAB**.</span></span> 
  
<span data-ttu-id="77781-119">Clientes e provedores não precisará chamar o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para tornar a alteração PAB permanente.</span><span class="sxs-lookup"><span data-stu-id="77781-119">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the PAB change permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="77781-120">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="77781-120">MFCMAPI reference</span></span>

<span data-ttu-id="77781-121">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="77781-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="77781-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="77781-122">**File**</span></span>|<span data-ttu-id="77781-123">**Function**</span><span class="sxs-lookup"><span data-stu-id="77781-123">**Function**</span></span>|<span data-ttu-id="77781-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="77781-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="77781-125">AbContDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="77781-125">AbContDlg.cpp</span></span>  <br/> |<span data-ttu-id="77781-126">CAbContDlg::OnSetPAB</span><span class="sxs-lookup"><span data-stu-id="77781-126">CAbContDlg::OnSetPAB</span></span>  <br/> |<span data-ttu-id="77781-127">MFCMAPI usa o método **SetPAB** para tornar o contêiner especificado do PAB.</span><span class="sxs-lookup"><span data-stu-id="77781-127">MFCMAPI uses the **SetPAB** method to make the specified container the PAB.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77781-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="77781-128">See also</span></span>



[<span data-ttu-id="77781-129">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="77781-129">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="77781-130">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="77781-130">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="77781-131">Propriedade canônica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="77781-131">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="77781-132">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="77781-132">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="77781-133">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="77781-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

