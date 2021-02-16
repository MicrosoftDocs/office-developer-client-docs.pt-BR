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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424613"
---
# <a name="iaddrbooksetpab"></a><span data-ttu-id="9202b-103">IAddrBook::SetPAB</span><span class="sxs-lookup"><span data-stu-id="9202b-103">IAddrBook::SetPAB</span></span>

  
  
<span data-ttu-id="9202b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9202b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9202b-105">Designa um contêiner específico como o pab (lista de endereços pessoal).</span><span class="sxs-lookup"><span data-stu-id="9202b-105">Designates a particular container as the personal address book (PAB).</span></span>
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="9202b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9202b-106">Parameters</span></span>

 <span data-ttu-id="9202b-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="9202b-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="9202b-108">[in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="9202b-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="9202b-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="9202b-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="9202b-110">[in] Um ponteiro para o identificador de entrada do contêiner a ser designado como o PAB.</span><span class="sxs-lookup"><span data-stu-id="9202b-110">[in] A pointer to the entry identifier of the container to be designated as the PAB.</span></span> <span data-ttu-id="9202b-111">O  _parâmetro lpEntryID_ não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="9202b-111">The  _lpEntryID_ parameter cannot be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9202b-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9202b-112">Return value</span></span>

<span data-ttu-id="9202b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="9202b-113">S_OK</span></span> 
  
> <span data-ttu-id="9202b-114">O contêiner especificado foi estabelecido como o PAB.</span><span class="sxs-lookup"><span data-stu-id="9202b-114">The specified container has been established as the PAB.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9202b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9202b-115">Remarks</span></span>

<span data-ttu-id="9202b-116">Os clientes e provedores de serviços chamam **o método SetPAB** para designar um contêiner específico como a PAB.</span><span class="sxs-lookup"><span data-stu-id="9202b-116">Clients and service providers call the **SetPAB** method to designate a particular container as the PAB.</span></span> <span data-ttu-id="9202b-117">A PAB é um contêiner que consiste em entradas copiadas de outros contêineres, bem como novas entradas.</span><span class="sxs-lookup"><span data-stu-id="9202b-117">The PAB is a container that consists of entries copied from other containers as well as new entries.</span></span> 
  
<span data-ttu-id="9202b-118">Uma chamada para **SetPAB** estabelece um contêiner como o PAB até que esse contêiner se torne indisponível ou um novo contêiner se torne o PAB por meio de uma chamada subsequente para **SetPAB**.</span><span class="sxs-lookup"><span data-stu-id="9202b-118">A call to **SetPAB** establishes a container as the PAB until that container is made unavailable or a new container becomes the PAB through a subsequent call to **SetPAB**.</span></span> 
  
<span data-ttu-id="9202b-119">Os clientes e provedores não têm que chamar o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para tornar a alteração de PAB permanente.</span><span class="sxs-lookup"><span data-stu-id="9202b-119">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the PAB change permanent.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9202b-120">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9202b-120">MFCMAPI reference</span></span>

<span data-ttu-id="9202b-121">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9202b-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9202b-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="9202b-122">**File**</span></span>|<span data-ttu-id="9202b-123">**Função**</span><span class="sxs-lookup"><span data-stu-id="9202b-123">**Function**</span></span>|<span data-ttu-id="9202b-124">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="9202b-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9202b-125">AbContDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9202b-125">AbContDlg.cpp</span></span>  <br/> |<span data-ttu-id="9202b-126">CAbContDlg::OnSetPAB</span><span class="sxs-lookup"><span data-stu-id="9202b-126">CAbContDlg::OnSetPAB</span></span>  <br/> |<span data-ttu-id="9202b-127">MFCMAPI usa o **método SetPAB** para tornar o contêiner especificado o PAB.</span><span class="sxs-lookup"><span data-stu-id="9202b-127">MFCMAPI uses the **SetPAB** method to make the specified container the PAB.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9202b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="9202b-128">See also</span></span>



[<span data-ttu-id="9202b-129">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="9202b-129">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="9202b-130">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="9202b-130">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="9202b-131">Propriedade canônica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="9202b-131">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="9202b-132">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9202b-132">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="9202b-133">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="9202b-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

