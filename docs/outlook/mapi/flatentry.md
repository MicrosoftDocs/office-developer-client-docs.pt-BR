---
title: FLATENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRY
api_type:
- COM
ms.assetid: 03e53e08-9113-4101-84c9-ccf6d43127f6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cf84c7d94e67da0ce7453829042e7be0d4e313f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585546"
---
# <a name="flatentry"></a><span data-ttu-id="1ba35-103">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="1ba35-103">FLATENTRY</span></span>

  
  
<span data-ttu-id="1ba35-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ba35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ba35-105">Uma estrutura [ENTRYID](entryid.md) mais uma contagem de bytes que especifica o tamanho da estrutura **ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="1ba35-105">An [ENTRYID](entryid.md) structure plus a byte count that specifies the size of the **ENTRYID** structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ba35-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1ba35-106">Header file:</span></span>  <br/> |<span data-ttu-id="1ba35-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ba35-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1ba35-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="1ba35-108">Related macros:</span></span>  <br/> |<span data-ttu-id="1ba35-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="1ba35-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a><span data-ttu-id="1ba35-110">Members</span><span class="sxs-lookup"><span data-stu-id="1ba35-110">Members</span></span>

 <span data-ttu-id="1ba35-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="1ba35-111">**cb**</span></span>
  
> <span data-ttu-id="1ba35-112">Contagem de bytes no membro **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="1ba35-112">Count of bytes in the **abEntry** member.</span></span> 
    
 <span data-ttu-id="1ba35-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="1ba35-113">**abEntry**</span></span>
  
> <span data-ttu-id="1ba35-114">O identificador de entrada completa que inclui a matriz de sinalizadores e dados binários.</span><span class="sxs-lookup"><span data-stu-id="1ba35-114">The complete entry identifier that includes the array of flags and binary data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ba35-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ba35-115">Remarks</span></span>

<span data-ttu-id="1ba35-116">Uma estrutura **FLATENTRY** é semelhante a uma estrutura [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="1ba35-116">A **FLATENTRY** structure resembles an [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="1ba35-117">No entanto, há algumas diferenças:</span><span class="sxs-lookup"><span data-stu-id="1ba35-117">However, there are some differences:</span></span> 
  
- <span data-ttu-id="1ba35-118">Uma estrutura **FLATENTRY** armazena o tamanho do identificador de entrada; Não suporta **ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="1ba35-118">A **FLATENTRY** structure stores the size of the entry identifier; **ENTRYID** does not.</span></span> 
    
- <span data-ttu-id="1ba35-119">Uma estrutura **FLATENTRY** armazena os dados de sinalizador junto com o restante do identificador de entrada; **ENTRYID** armazenando-as separadamente.</span><span class="sxs-lookup"><span data-stu-id="1ba35-119">A **FLATENTRY** structure stores the flag data together with the rest of the entry identifier; **ENTRYID** stores them separately.</span></span> 
    
- <span data-ttu-id="1ba35-120">Uma estrutura **FLATENTRY** é usada para armazenar um identificador de entrada em um arquivo ou passá-la em um fluxo de bytes, enquanto uma estrutura **ENTRYID** é usada pelos métodos interface [IMAPIProp](imapipropiunknown.md) e pelos seguintes métodos **OpenEntry** : [IABLogon: : OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="1ba35-120">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes whereas an **ENTRYID** structure is used by the [IMAPIProp](imapipropiunknown.md) interface methods and by the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="1ba35-121">Uma estrutura **FLATENTRY** é usada para armazenar um identificador de entrada em um arquivo ou passá-la em um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="1ba35-121">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> <span data-ttu-id="1ba35-122">Uma estrutura **ENTRYID** é usada para armazenar um identificador de entrada no disco.</span><span class="sxs-lookup"><span data-stu-id="1ba35-122">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1ba35-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ba35-123">See also</span></span>



[<span data-ttu-id="1ba35-124">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1ba35-124">ENTRYID</span></span>](entryid.md)


[<span data-ttu-id="1ba35-125">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="1ba35-125">MAPI Structures</span></span>](mapi-structures.md)

