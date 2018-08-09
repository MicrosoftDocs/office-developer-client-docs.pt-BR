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
ms.openlocfilehash: 3d67d71effde87711e3be9aca1b979627acda37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766881"
---
# <a name="iaddrbookgetpab"></a><span data-ttu-id="77c0a-103">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="77c0a-103">IAddrBook::GetPAB</span></span>

  
  
<span data-ttu-id="77c0a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="77c0a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="77c0a-105">Retorna o identificador de entrada do contêiner que é designado como o catálogo de endereços pessoal (PAB).</span><span class="sxs-lookup"><span data-stu-id="77c0a-105">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="77c0a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77c0a-106">Parameters</span></span>

 <span data-ttu-id="77c0a-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="77c0a-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="77c0a-108">[out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="77c0a-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="77c0a-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="77c0a-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="77c0a-110">[out] Um ponteiro para um ponteiro para o identificador de entrada do PAB.</span><span class="sxs-lookup"><span data-stu-id="77c0a-110">[out] A pointer to a pointer to the entry identifier of the PAB.</span></span> <span data-ttu-id="77c0a-111">O parâmetro _lppEntryID_ contém zero se nenhum contêiner foi designada como o PAB.</span><span class="sxs-lookup"><span data-stu-id="77c0a-111">The  _lppEntryID_ parameter contains zero if no container has been designated as the PAB.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="77c0a-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="77c0a-112">Return value</span></span>

<span data-ttu-id="77c0a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="77c0a-113">S_OK</span></span> 
  
> <span data-ttu-id="77c0a-114">O identificador de entrada do PAB foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="77c0a-114">The entry identifier of the PAB was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77c0a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="77c0a-115">Remarks</span></span>

<span data-ttu-id="77c0a-116">Clientes chamar o método **GetPAB** para recuperar o identificador de entrada do contêiner designado como o PAB.</span><span class="sxs-lookup"><span data-stu-id="77c0a-116">Clients call the **GetPAB** method to retrieve the entry identifier of the container designated as the PAB.</span></span> <span data-ttu-id="77c0a-117">Se um PAB não tiver sido estabelecido no perfil, MAPI selecionará como o PAB o primeiro contêiner na hierarquia de catálogo de endereços que permite modificações.</span><span class="sxs-lookup"><span data-stu-id="77c0a-117">If a PAB has not been established in the profile, MAPI selects as the PAB the first container in the address book hierarchy that allows modifications.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="77c0a-118">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="77c0a-118">MFCMAPI reference</span></span>

<span data-ttu-id="77c0a-119">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="77c0a-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="77c0a-120">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="77c0a-120">**File**</span></span>|<span data-ttu-id="77c0a-121">**Function**</span><span class="sxs-lookup"><span data-stu-id="77c0a-121">**Function**</span></span>|<span data-ttu-id="77c0a-122">**Comment**</span><span class="sxs-lookup"><span data-stu-id="77c0a-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="77c0a-123">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="77c0a-123">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="77c0a-124">CMainDlg::OnOpenPAB</span><span class="sxs-lookup"><span data-stu-id="77c0a-124">CMainDlg::OnOpenPAB</span></span>  <br/> |<span data-ttu-id="77c0a-125">MFCMAPI usa o método **GetPAB** para obter a ID do catálogo de endereços pessoal do usuário.</span><span class="sxs-lookup"><span data-stu-id="77c0a-125">MFCMAPI uses the **GetPAB** method to get the ID for the user's personal address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77c0a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="77c0a-126">See also</span></span>



[<span data-ttu-id="77c0a-127">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="77c0a-127">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="77c0a-128">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="77c0a-128">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="77c0a-129">Propriedade canônica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="77c0a-129">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="77c0a-130">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="77c0a-130">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="77c0a-131">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="77c0a-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

