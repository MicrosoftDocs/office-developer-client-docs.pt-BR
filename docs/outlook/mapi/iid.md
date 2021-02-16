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
ms.openlocfilehash: 5605de7dbcc18197748713bcf909839690d7259f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411593"
---
# <a name="iid"></a><span data-ttu-id="af0ce-103">IID</span><span class="sxs-lookup"><span data-stu-id="af0ce-103">IID</span></span>

  
  
<span data-ttu-id="af0ce-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af0ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af0ce-105">Descreve uma estrutura [GUID](guid.md) usada para descrever um identificador para uma interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="af0ce-105">Describes a [GUID](guid.md) structure used to describe an identifier for a MAPI interface.</span></span> 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="af0ce-106">Members</span><span class="sxs-lookup"><span data-stu-id="af0ce-106">Members</span></span>

<span data-ttu-id="af0ce-107">Consulte a estrutura **guid.**</span><span class="sxs-lookup"><span data-stu-id="af0ce-107">See the **GUID** structure.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="af0ce-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="af0ce-108">Remarks</span></span>

<span data-ttu-id="af0ce-109">Uma **estrutura IID** é usada para identificar exclusivamente uma interface MAPI e associar uma interface específica a um objeto.</span><span class="sxs-lookup"><span data-stu-id="af0ce-109">An **IID** structure is used to uniquely identify a MAPI interface and to associate a particular interface with an object.</span></span> <span data-ttu-id="af0ce-110">Por exemplo, quando um cliente chama [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir uma pasta, o cliente define o parâmetro _lpInterface_ para apontar para um **IID** que representa a interface [IMAPIFolder.](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="af0ce-110">For example, when a client calls [IMAPISession::OpenEntry](imapisession-openentry.md) to open a folder, the client sets the  _lpInterface_ parameter to point to an **IID** representing the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> <span data-ttu-id="af0ce-111">MAPI define o **IMAPIFolderIID** a ser IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="af0ce-111">MAPI defines the **IMAPIFolderIID** to be IID_IMAPIFolder.</span></span> <span data-ttu-id="af0ce-112">**Estruturas IID** também são usadas para identificar exclusivamente interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="af0ce-112">**IID** structures are also used to uniquely identify OLE interfaces.</span></span> 
  
<span data-ttu-id="af0ce-113">Todas as estruturas **de IID específicas** para as interfaces MAPI são definidas no arquivo de header Mapiguid.h.</span><span class="sxs-lookup"><span data-stu-id="af0ce-113">All of the specific **IID** structures for the MAPI interfaces are defined in the Mapiguid.h header file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="af0ce-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="af0ce-114">See also</span></span>



[<span data-ttu-id="af0ce-115">GUID</span><span class="sxs-lookup"><span data-stu-id="af0ce-115">GUID</span></span>](guid.md)


[<span data-ttu-id="af0ce-116">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="af0ce-116">MAPI Structures</span></span>](mapi-structures.md)

