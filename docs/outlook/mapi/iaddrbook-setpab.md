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
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287011"
---
# <a name="iaddrbooksetpab"></a><span data-ttu-id="56a56-103">IAddrBook::SetPAB</span><span class="sxs-lookup"><span data-stu-id="56a56-103">IAddrBook::SetPAB</span></span>

  
  
<span data-ttu-id="56a56-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56a56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56a56-105">Designa um determinado contêiner como o catálogo de endereços pessoal (PAB).</span><span class="sxs-lookup"><span data-stu-id="56a56-105">Designates a particular container as the personal address book (PAB).</span></span>
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="56a56-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56a56-106">Parameters</span></span>

 <span data-ttu-id="56a56-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="56a56-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="56a56-108">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="56a56-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="56a56-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="56a56-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="56a56-110">no Um ponteiro para o identificador de entrada do contêiner a ser designado como o PAB.</span><span class="sxs-lookup"><span data-stu-id="56a56-110">[in] A pointer to the entry identifier of the container to be designated as the PAB.</span></span> <span data-ttu-id="56a56-111">O parâmetro _lpEntryID_ não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="56a56-111">The  _lpEntryID_ parameter cannot be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="56a56-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="56a56-112">Return value</span></span>

<span data-ttu-id="56a56-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="56a56-113">S_OK</span></span> 
  
> <span data-ttu-id="56a56-114">O contêiner especificado foi estabelecido como o PAB.</span><span class="sxs-lookup"><span data-stu-id="56a56-114">The specified container has been established as the PAB.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="56a56-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="56a56-115">Remarks</span></span>

<span data-ttu-id="56a56-116">Os clientes e os provedores de serviços chamam o método **SetPAB** para designar um determinado contêiner como o PAB.</span><span class="sxs-lookup"><span data-stu-id="56a56-116">Clients and service providers call the **SetPAB** method to designate a particular container as the PAB.</span></span> <span data-ttu-id="56a56-117">O PAB é um contêiner que consiste em entradas copiadas de outros contêineres, bem como novas entradas.</span><span class="sxs-lookup"><span data-stu-id="56a56-117">The PAB is a container that consists of entries copied from other containers as well as new entries.</span></span> 
  
<span data-ttu-id="56a56-118">Uma chamada para **SetPAB** estabelece um contêiner como o PAB até que esse contêiner seja tornado indisponível ou um novo contêiner se torne o PAB por meio de uma chamada subsequente para o **SetPAB**.</span><span class="sxs-lookup"><span data-stu-id="56a56-118">A call to **SetPAB** establishes a container as the PAB until that container is made unavailable or a new container becomes the PAB through a subsequent call to **SetPAB**.</span></span> 
  
<span data-ttu-id="56a56-119">Os clientes e provedores não precisam chamar o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) para tornar o PAB alterado permanentemente.</span><span class="sxs-lookup"><span data-stu-id="56a56-119">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the PAB change permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="56a56-120">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="56a56-120">MFCMAPI reference</span></span>

<span data-ttu-id="56a56-121">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="56a56-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="56a56-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="56a56-122">**File**</span></span>|<span data-ttu-id="56a56-123">**Função**</span><span class="sxs-lookup"><span data-stu-id="56a56-123">**Function**</span></span>|<span data-ttu-id="56a56-124">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="56a56-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="56a56-125">AbContDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="56a56-125">AbContDlg.cpp</span></span>  <br/> |<span data-ttu-id="56a56-126">CAbContDlg:: OnSetPAB</span><span class="sxs-lookup"><span data-stu-id="56a56-126">CAbContDlg::OnSetPAB</span></span>  <br/> |<span data-ttu-id="56a56-127">MFCMAPI usa o método **SetPAB** para tornar o contêiner especificado o PAB.</span><span class="sxs-lookup"><span data-stu-id="56a56-127">MFCMAPI uses the **SetPAB** method to make the specified container the PAB.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="56a56-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="56a56-128">See also</span></span>



[<span data-ttu-id="56a56-129">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="56a56-129">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="56a56-130">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="56a56-130">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="56a56-131">Propriedade canônica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="56a56-131">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="56a56-132">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="56a56-132">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="56a56-133">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="56a56-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

