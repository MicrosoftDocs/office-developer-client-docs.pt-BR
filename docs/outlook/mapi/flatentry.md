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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 2f5f4d50b085c437d1caab5f70dcb741afe090bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766561"
---
# <a name="flatentry"></a><span data-ttu-id="4b68c-103">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="4b68c-103">FLATENTRY</span></span>

  
  
<span data-ttu-id="4b68c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4b68c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4b68c-105">Uma estrutura [ENTRYID](entryid.md) mais uma contagem de bytes que especifica o tamanho da estrutura **ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="4b68c-105">An [ENTRYID](entryid.md) structure plus a byte count that specifies the size of the **ENTRYID** structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b68c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4b68c-106">Header file:</span></span>  <br/> |<span data-ttu-id="4b68c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b68c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4b68c-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="4b68c-108">Related macros:</span></span>  <br/> |<span data-ttu-id="4b68c-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span><span class="sxs-lookup"><span data-stu-id="4b68c-109">[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a><span data-ttu-id="4b68c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="4b68c-110">Members</span></span>

 <span data-ttu-id="4b68c-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="4b68c-111">**cb**</span></span>
  
> <span data-ttu-id="4b68c-112">Contagem de bytes no membro **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="4b68c-112">Count of bytes in the **abEntry** member.</span></span> 
    
 <span data-ttu-id="4b68c-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="4b68c-113">**abEntry**</span></span>
  
> <span data-ttu-id="4b68c-114">O identificador de entrada completa que inclui a matriz de sinalizadores e dados binários.</span><span class="sxs-lookup"><span data-stu-id="4b68c-114">The complete entry identifier that includes the array of flags and binary data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b68c-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="4b68c-115">Remarks</span></span>

<span data-ttu-id="4b68c-116">Uma estrutura **FLATENTRY** é semelhante a uma estrutura [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="4b68c-116">A **FLATENTRY** structure resembles an [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="4b68c-117">No entanto, há algumas diferenças:</span><span class="sxs-lookup"><span data-stu-id="4b68c-117">However, there are some differences:</span></span> 
  
- <span data-ttu-id="4b68c-118">Uma estrutura **FLATENTRY** armazena o tamanho do identificador de entrada; Não suporta **ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="4b68c-118">A **FLATENTRY** structure stores the size of the entry identifier; **ENTRYID** does not.</span></span> 
    
- <span data-ttu-id="4b68c-119">Uma estrutura **FLATENTRY** armazena os dados de sinalizador junto com o restante do identificador de entrada; **ENTRYID** armazenando-as separadamente.</span><span class="sxs-lookup"><span data-stu-id="4b68c-119">A **FLATENTRY** structure stores the flag data together with the rest of the entry identifier; **ENTRYID** stores them separately.</span></span> 
    
- <span data-ttu-id="4b68c-120">Uma estrutura **FLATENTRY** é usada para armazenar um identificador de entrada em um arquivo ou passá-la em um fluxo de bytes, enquanto uma estrutura **ENTRYID** é usada pelos métodos interface [IMAPIProp](imapipropiunknown.md) e pelos seguintes métodos **OpenEntry** : [IABLogon: : OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="4b68c-120">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes whereas an **ENTRYID** structure is used by the [IMAPIProp](imapipropiunknown.md) interface methods and by the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="4b68c-121">Uma estrutura **FLATENTRY** é usada para armazenar um identificador de entrada em um arquivo ou passá-la em um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="4b68c-121">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> <span data-ttu-id="4b68c-122">Uma estrutura **ENTRYID** é usada para armazenar um identificador de entrada no disco.</span><span class="sxs-lookup"><span data-stu-id="4b68c-122">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4b68c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b68c-123">See also</span></span>



[<span data-ttu-id="4b68c-124">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4b68c-124">ENTRYID</span></span>](entryid.md)


[<span data-ttu-id="4b68c-125">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="4b68c-125">MAPI Structures</span></span>](mapi-structures.md)

