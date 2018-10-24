---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 00c7560427ece58026030ce6895d60aec7cc5a2e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570937"
---
# <a name="iid"></a><span data-ttu-id="c56a6-103">IID</span><span class="sxs-lookup"><span data-stu-id="c56a6-103">IID</span></span>

  
  
<span data-ttu-id="c56a6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c56a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c56a6-105">Descreve uma estrutura [GUID](guid.md) usada para descrever um identificador para uma interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="c56a6-105">Describes a [GUID](guid.md) structure used to describe an identifier for a MAPI interface.</span></span> 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="c56a6-106">Members</span><span class="sxs-lookup"><span data-stu-id="c56a6-106">Members</span></span>

<span data-ttu-id="c56a6-107">Ver a estrutura **GUID** .</span><span class="sxs-lookup"><span data-stu-id="c56a6-107">See the **GUID** structure.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c56a6-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="c56a6-108">Remarks</span></span>

<span data-ttu-id="c56a6-109">Uma estrutura **IID** é usada para identificar exclusivamente uma interface MAPI e para associar a um objeto de uma determinada interface.</span><span class="sxs-lookup"><span data-stu-id="c56a6-109">An **IID** structure is used to uniquely identify a MAPI interface and to associate a particular interface with an object.</span></span> <span data-ttu-id="c56a6-110">Por exemplo, quando um cliente chamadas [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir uma pasta, o cliente define o parâmetro _lpInterface_ para apontar para um **IID** representando a interface [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="c56a6-110">For example, when a client calls [IMAPISession::OpenEntry](imapisession-openentry.md) to open a folder, the client sets the  _lpInterface_ parameter to point to an **IID** representing the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> <span data-ttu-id="c56a6-111">MAPI define o **IMAPIFolderIID** para ser IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="c56a6-111">MAPI defines the **IMAPIFolderIID** to be IID_IMAPIFolder.</span></span> <span data-ttu-id="c56a6-112">Estruturas **IID** também são usadas para identificar exclusivamente interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="c56a6-112">**IID** structures are also used to uniquely identify OLE interfaces.</span></span> 
  
<span data-ttu-id="c56a6-113">Todas as estruturas **IID** específicas para as interfaces de MAPI são definidas no arquivo de cabeçalho Mapiguid.h.</span><span class="sxs-lookup"><span data-stu-id="c56a6-113">All of the specific **IID** structures for the MAPI interfaces are defined in the Mapiguid.h header file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c56a6-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="c56a6-114">See also</span></span>



[<span data-ttu-id="c56a6-115">GUID</span><span class="sxs-lookup"><span data-stu-id="c56a6-115">GUID</span></span>](guid.md)


[<span data-ttu-id="c56a6-116">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="c56a6-116">MAPI Structures</span></span>](mapi-structures.md)

