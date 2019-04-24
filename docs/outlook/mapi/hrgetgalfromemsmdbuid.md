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
ms.openlocfilehash: b9a31fec93ec7fafc4d1565d63e4bc427ba4050e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347828"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="85adf-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="85adf-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="85adf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85adf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85adf-105">Retorna o identificador de entrada do catálogo de endereços global para o serviço do Exchange identificado por _pEmsmdbUID_.</span><span class="sxs-lookup"><span data-stu-id="85adf-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="85adf-106">O identificador de entrada retornado deve ser liberado usando [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="85adf-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="85adf-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="85adf-107">Header file:</span></span>  <br/> |<span data-ttu-id="85adf-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="85adf-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="85adf-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="85adf-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="85adf-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="85adf-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="85adf-111">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="85adf-111">Called by:</span></span>  <br/> |<span data-ttu-id="85adf-112">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="85adf-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="85adf-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85adf-113">Parameters</span></span>

 <span data-ttu-id="85adf-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="85adf-114">_pSess_</span></span>
  
> <span data-ttu-id="85adf-115">no O IMAPISession conectado.</span><span class="sxs-lookup"><span data-stu-id="85adf-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="85adf-116">Ele não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="85adf-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="85adf-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="85adf-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="85adf-118">no O catálogo de endereços usado para abrir o identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="85adf-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="85adf-119">Ele não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="85adf-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="85adf-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="85adf-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="85adf-121">no Um ponteiro para um **emsmdbUID** que identifica a GAL do serviço do Exchange a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="85adf-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="85adf-122">Se _pEmsmdbUID_ for nulo ou a UID zero, essa função obterá a GAL herdada do serviço do Exchange.</span><span class="sxs-lookup"><span data-stu-id="85adf-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="85adf-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="85adf-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="85adf-124">bota Um ponteiro para o número de bytes do identificador de entrada da lista de endereços global.</span><span class="sxs-lookup"><span data-stu-id="85adf-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="85adf-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="85adf-125">_lppeid_</span></span>
  
> <span data-ttu-id="85adf-126">bota Um ponteiro para o identificador de entrada da lista de endereços global.</span><span class="sxs-lookup"><span data-stu-id="85adf-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="85adf-127">Isso deve ser liberado usando o [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="85adf-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

