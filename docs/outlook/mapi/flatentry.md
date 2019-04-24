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
ms.openlocfilehash: e47f4e0d1ab9ab3ecfd53932b8ef26440134c603
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334815"
---
# <a name="flatentry"></a><span data-ttu-id="84939-103">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="84939-103">FLATENTRY</span></span>

  
  
<span data-ttu-id="84939-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84939-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84939-105">Uma [](entryid.md) estrutura ENTRYID mais uma contagem de bytes que especifica o tamanho da \*\*\*\* estrutura ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="84939-105">An [ENTRYID](entryid.md) structure plus a byte count that specifies the size of the **ENTRYID** structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84939-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="84939-106">Header file:</span></span>  <br/> |<span data-ttu-id="84939-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="84939-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="84939-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="84939-108">Related macros:</span></span>  <br/> |<span data-ttu-id="84939-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="84939-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a><span data-ttu-id="84939-110">Members</span><span class="sxs-lookup"><span data-stu-id="84939-110">Members</span></span>

 <span data-ttu-id="84939-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="84939-111">**cb**</span></span>
  
> <span data-ttu-id="84939-112">Contagem de bytes no membro **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="84939-112">Count of bytes in the **abEntry** member.</span></span> 
    
 <span data-ttu-id="84939-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="84939-113">**abEntry**</span></span>
  
> <span data-ttu-id="84939-114">O identificador de entrada completo que inclui a matriz de sinalizadores e dados binários.</span><span class="sxs-lookup"><span data-stu-id="84939-114">The complete entry identifier that includes the array of flags and binary data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="84939-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="84939-115">Remarks</span></span>

<span data-ttu-id="84939-116">Uma estrutura **FLATENTRY** lembra de uma estrutura [EntryID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="84939-116">A **FLATENTRY** structure resembles an [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="84939-117">No enTanto, há algumas diferenças:</span><span class="sxs-lookup"><span data-stu-id="84939-117">However, there are some differences:</span></span> 
  
- <span data-ttu-id="84939-118">Uma estrutura **FLATENTRY** armazena o tamanho do identificador de entrada; **EntryID** não.</span><span class="sxs-lookup"><span data-stu-id="84939-118">A **FLATENTRY** structure stores the size of the entry identifier; **ENTRYID** does not.</span></span> 
    
- <span data-ttu-id="84939-119">Uma estrutura **FLATENTRY** armazena os dados de sinalizador junto com o resto do identificador de entrada; **EntryID** as armazena separadamente.</span><span class="sxs-lookup"><span data-stu-id="84939-119">A **FLATENTRY** structure stores the flag data together with the rest of the entry identifier; **ENTRYID** stores them separately.</span></span> 
    
- <span data-ttu-id="84939-120">Uma estrutura **FLATENTRY** é usada para armazenar um identificador de entrada em um arquivo ou passá-lo em um fluxo de bytes, enquanto uma estrutura **EntryID** é usada pelos métodos da interface [IMAPIProp](imapipropiunknown.md) e pelos seguintes métodos de **OpenEntry** : [IABLogon: : OpenEntry](iablogon-openentry.md), [IAddrBook:: OpenEntry](iaddrbook-openentry.md), [IMAPIContainer:](imapicontainer-openentry.md): OpenEntry, [IMAPISession:](imapisession-openentry.md): OpenEntry, [](imapisupport-openentry.md)IMAPISupport [:](imsgstore-openentry.md)OpenEntry, IMsgStore:: OpenEntry [](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="84939-120">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes whereas an **ENTRYID** structure is used by the [IMAPIProp](imapipropiunknown.md) interface methods and by the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="84939-121">Uma estrutura **FLATENTRY** é usada para armazenar um identificador de entrada em um arquivo ou passá-lo em um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="84939-121">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> <span data-ttu-id="84939-122">Uma \*\*\*\* estrutura ENTRYID é usada para armazenar um identificador de entrada no disco.</span><span class="sxs-lookup"><span data-stu-id="84939-122">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="84939-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="84939-123">See also</span></span>



[<span data-ttu-id="84939-124">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="84939-124">ENTRYID</span></span>](entryid.md)


[<span data-ttu-id="84939-125">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="84939-125">MAPI Structures</span></span>](mapi-structures.md)

