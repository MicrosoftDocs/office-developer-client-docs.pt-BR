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
ms.openlocfilehash: 1f93ee653c9365488432c4e797b171a199c30107
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583712"
---
# <a name="iaddrbookgetpab"></a><span data-ttu-id="677c0-103">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="677c0-103">IAddrBook::GetPAB</span></span>

  
  
<span data-ttu-id="677c0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="677c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="677c0-105">Retorna o identificador de entrada do contêiner que é designado como o catálogo de endereços pessoal (PAB).</span><span class="sxs-lookup"><span data-stu-id="677c0-105">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="677c0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="677c0-106">Parameters</span></span>

 <span data-ttu-id="677c0-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="677c0-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="677c0-108">[out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="677c0-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="677c0-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="677c0-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="677c0-110">[out] Um ponteiro para um ponteiro para o identificador de entrada do PAB.</span><span class="sxs-lookup"><span data-stu-id="677c0-110">[out] A pointer to a pointer to the entry identifier of the PAB.</span></span> <span data-ttu-id="677c0-111">O parâmetro _lppEntryID_ contém zero se nenhum contêiner foi designada como o PAB.</span><span class="sxs-lookup"><span data-stu-id="677c0-111">The  _lppEntryID_ parameter contains zero if no container has been designated as the PAB.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="677c0-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="677c0-112">Return value</span></span>

<span data-ttu-id="677c0-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="677c0-113">S_OK</span></span> 
  
> <span data-ttu-id="677c0-114">O identificador de entrada do PAB foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="677c0-114">The entry identifier of the PAB was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="677c0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="677c0-115">Remarks</span></span>

<span data-ttu-id="677c0-116">Clientes chamar o método **GetPAB** para recuperar o identificador de entrada do contêiner designado como o PAB.</span><span class="sxs-lookup"><span data-stu-id="677c0-116">Clients call the **GetPAB** method to retrieve the entry identifier of the container designated as the PAB.</span></span> <span data-ttu-id="677c0-117">Se um PAB não tiver sido estabelecido no perfil, MAPI selecionará como o PAB o primeiro contêiner na hierarquia de catálogo de endereços que permite modificações.</span><span class="sxs-lookup"><span data-stu-id="677c0-117">If a PAB has not been established in the profile, MAPI selects as the PAB the first container in the address book hierarchy that allows modifications.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="677c0-118">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="677c0-118">MFCMAPI reference</span></span>

<span data-ttu-id="677c0-119">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="677c0-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="677c0-120">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="677c0-120">**File**</span></span>|<span data-ttu-id="677c0-121">**Function**</span><span class="sxs-lookup"><span data-stu-id="677c0-121">**Function**</span></span>|<span data-ttu-id="677c0-122">**Comment**</span><span class="sxs-lookup"><span data-stu-id="677c0-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="677c0-123">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="677c0-123">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="677c0-124">CMainDlg::OnOpenPAB</span><span class="sxs-lookup"><span data-stu-id="677c0-124">CMainDlg::OnOpenPAB</span></span>  <br/> |<span data-ttu-id="677c0-125">MFCMAPI usa o método **GetPAB** para obter a ID do catálogo de endereços pessoal do usuário.</span><span class="sxs-lookup"><span data-stu-id="677c0-125">MFCMAPI uses the **GetPAB** method to get the ID for the user's personal address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="677c0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="677c0-126">See also</span></span>



[<span data-ttu-id="677c0-127">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="677c0-127">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="677c0-128">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="677c0-128">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="677c0-129">Propriedade canônica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="677c0-129">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="677c0-130">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="677c0-130">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="677c0-131">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="677c0-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

