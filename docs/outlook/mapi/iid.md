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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a0e859ac0f8bcc3bd83e336c85da21f1251efcb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766926"
---
# <a name="iid"></a><span data-ttu-id="51336-103">IID</span><span class="sxs-lookup"><span data-stu-id="51336-103">IID</span></span>

  
  
<span data-ttu-id="51336-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51336-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51336-105">Descreve uma estrutura [GUID](guid.md) usada para descrever um identificador para uma interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="51336-105">Describes a [GUID](guid.md) structure used to describe an identifier for a MAPI interface.</span></span> 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="51336-106">Members</span><span class="sxs-lookup"><span data-stu-id="51336-106">Members</span></span>

<span data-ttu-id="51336-107">Ver a estrutura **GUID** .</span><span class="sxs-lookup"><span data-stu-id="51336-107">See the **GUID** structure.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="51336-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="51336-108">Remarks</span></span>

<span data-ttu-id="51336-109">Uma estrutura **IID** é usada para identificar exclusivamente uma interface MAPI e para associar a um objeto de uma determinada interface.</span><span class="sxs-lookup"><span data-stu-id="51336-109">An **IID** structure is used to uniquely identify a MAPI interface and to associate a particular interface with an object.</span></span> <span data-ttu-id="51336-110">Por exemplo, quando um cliente chamadas [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir uma pasta, o cliente define o parâmetro _lpInterface_ para apontar para um **IID** representando a interface [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="51336-110">For example, when a client calls [IMAPISession::OpenEntry](imapisession-openentry.md) to open a folder, the client sets the  _lpInterface_ parameter to point to an **IID** representing the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> <span data-ttu-id="51336-111">MAPI define o **IMAPIFolderIID** para ser IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="51336-111">MAPI defines the **IMAPIFolderIID** to be IID_IMAPIFolder.</span></span> <span data-ttu-id="51336-112">Estruturas **IID** também são usadas para identificar exclusivamente interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="51336-112">**IID** structures are also used to uniquely identify OLE interfaces.</span></span> 
  
<span data-ttu-id="51336-113">Todas as estruturas **IID** específicas para as interfaces de MAPI são definidas no arquivo de cabeçalho Mapiguid.h.</span><span class="sxs-lookup"><span data-stu-id="51336-113">All of the specific **IID** structures for the MAPI interfaces are defined in the Mapiguid.h header file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="51336-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="51336-114">See also</span></span>



[<span data-ttu-id="51336-115">GUID</span><span class="sxs-lookup"><span data-stu-id="51336-115">GUID</span></span>](guid.md)


[<span data-ttu-id="51336-116">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="51336-116">MAPI Structures</span></span>](mapi-structures.md)

