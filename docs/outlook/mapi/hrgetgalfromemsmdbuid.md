---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5db1b45f42365837d7b0e7af91f859f221ff687b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766788"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="a4ac4-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="a4ac4-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="a4ac4-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a4ac4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a4ac4-105">Retorna o identificador de entrada do catálogo de endereços global para o serviço Exchange identificado pela _pEmsmdbUID_.</span><span class="sxs-lookup"><span data-stu-id="a4ac4-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="a4ac4-106">O identificador de entrada retornados deve ser liberado usando [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="a4ac4-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a4ac4-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a4ac4-107">Header file:</span></span>  <br/> |<span data-ttu-id="a4ac4-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="a4ac4-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="a4ac4-109">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="a4ac4-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="a4ac4-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="a4ac4-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="a4ac4-111">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="a4ac4-111">Called by:</span></span>  <br/> |<span data-ttu-id="a4ac4-112">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="a4ac4-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="a4ac4-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4ac4-113">Parameters</span></span>

 <span data-ttu-id="a4ac4-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="a4ac4-114">_pSess_</span></span>
  
> <span data-ttu-id="a4ac4-115">[in] O conectado IMAPISession.</span><span class="sxs-lookup"><span data-stu-id="a4ac4-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="a4ac4-116">Ele não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a4ac4-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="a4ac4-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="a4ac4-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="a4ac4-118">[in] O catálogo de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="a4ac4-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="a4ac4-119">Ele não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a4ac4-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="a4ac4-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="a4ac4-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="a4ac4-121">[in] Um ponteiro para uma **emsmdbUID** que identifica a GAL do serviço Exchange a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="a4ac4-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="a4ac4-122">Se _pEmsmdbUID_ for NULL ou o UID zero, essa função obtém a GAL herdada do serviço do Exchange.</span><span class="sxs-lookup"><span data-stu-id="a4ac4-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="a4ac4-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="a4ac4-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="a4ac4-124">[out] Um ponteiro para a contagem de bytes do identificador de entrada da lista de endereços global.</span><span class="sxs-lookup"><span data-stu-id="a4ac4-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="a4ac4-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="a4ac4-125">_lppeid_</span></span>
  
> <span data-ttu-id="a4ac4-126">[out] Um ponteiro para o identificador de entrada da lista de endereços global.</span><span class="sxs-lookup"><span data-stu-id="a4ac4-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="a4ac4-127">Isso deve ser liberado usando [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="a4ac4-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

