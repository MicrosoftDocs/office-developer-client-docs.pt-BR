---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6c565c088fd4ef7d5df141bf770c560f79535998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419895"
---
# <a name="iaddrbookgetpab"></a><span data-ttu-id="a07da-103">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="a07da-103">IAddrBook::GetPAB</span></span>

  
  
<span data-ttu-id="a07da-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a07da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a07da-105">Retorna o identificador de entrada do contêiner designado como o pab (lista de endereços pessoal).</span><span class="sxs-lookup"><span data-stu-id="a07da-105">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="a07da-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a07da-106">Parameters</span></span>

 <span data-ttu-id="a07da-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a07da-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="a07da-108">[out] Um ponteiro para a contagem de byte no identificador de entrada apontado pelo _parâmetro lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="a07da-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a07da-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="a07da-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="a07da-110">[out] Um ponteiro para um ponteiro para o identificador de entrada do PAB.</span><span class="sxs-lookup"><span data-stu-id="a07da-110">[out] A pointer to a pointer to the entry identifier of the PAB.</span></span> <span data-ttu-id="a07da-111">O  _parâmetro lppEntryID_ conterá zero se nenhum contêiner tiver sido designado como PAB.</span><span class="sxs-lookup"><span data-stu-id="a07da-111">The  _lppEntryID_ parameter contains zero if no container has been designated as the PAB.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a07da-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a07da-112">Return value</span></span>

<span data-ttu-id="a07da-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a07da-113">S_OK</span></span> 
  
> <span data-ttu-id="a07da-114">O identificador de entrada do PAB foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="a07da-114">The entry identifier of the PAB was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a07da-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a07da-115">Remarks</span></span>

<span data-ttu-id="a07da-116">Os clientes chamam **o método GetPAB** para recuperar o identificador de entrada do contêiner designado como PAB.</span><span class="sxs-lookup"><span data-stu-id="a07da-116">Clients call the **GetPAB** method to retrieve the entry identifier of the container designated as the PAB.</span></span> <span data-ttu-id="a07da-117">Se um PAB não tiver sido estabelecido no perfil, o MAPI selecionará como o PAB o primeiro contêiner na hierarquia do livro de endereços que permitirá modificações.</span><span class="sxs-lookup"><span data-stu-id="a07da-117">If a PAB has not been established in the profile, MAPI selects as the PAB the first container in the address book hierarchy that allows modifications.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a07da-118">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a07da-118">MFCMAPI reference</span></span>

<span data-ttu-id="a07da-119">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a07da-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a07da-120">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="a07da-120">**File**</span></span>|<span data-ttu-id="a07da-121">**Função**</span><span class="sxs-lookup"><span data-stu-id="a07da-121">**Function**</span></span>|<span data-ttu-id="a07da-122">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="a07da-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a07da-123">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a07da-123">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="a07da-124">CMainDlg::OnOpenPAB</span><span class="sxs-lookup"><span data-stu-id="a07da-124">CMainDlg::OnOpenPAB</span></span>  <br/> |<span data-ttu-id="a07da-125">MFCMAPI usa o **método GetPAB** para obter a ID do livro de endereços pessoal do usuário.</span><span class="sxs-lookup"><span data-stu-id="a07da-125">MFCMAPI uses the **GetPAB** method to get the ID for the user's personal address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a07da-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a07da-126">See also</span></span>



[<span data-ttu-id="a07da-127">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="a07da-127">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="a07da-128">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a07da-128">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a07da-129">Propriedade canônica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="a07da-129">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="a07da-130">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a07da-130">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="a07da-131">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="a07da-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

