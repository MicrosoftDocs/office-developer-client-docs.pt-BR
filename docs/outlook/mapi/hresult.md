---
title: HRESULT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: b248ed11-3d8a-4d4c-9b84-fa5bee7979c7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 64fcbebbd71bc3f478f36c711e49db9a3518ef9a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347793"
---
# <a name="hresult"></a><span data-ttu-id="45d81-103">HRESULT</span><span class="sxs-lookup"><span data-stu-id="45d81-103">HRESULT</span></span>

  
  
<span data-ttu-id="45d81-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45d81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45d81-105">Um valor de 32 bits usado para descrever um erro ou aviso.</span><span class="sxs-lookup"><span data-stu-id="45d81-105">A 32-bit value that is used to describe an error or warning.</span></span>
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a><span data-ttu-id="45d81-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="45d81-106">Remarks</span></span>

<span data-ttu-id="45d81-107">O tipo de dados **HRESULT** é o mesmo que o tipo de dados [SCODE](scode.md) .</span><span class="sxs-lookup"><span data-stu-id="45d81-107">The **HRESULT** data type is the same as the [SCODE](scode.md) data type.</span></span> 
  
<span data-ttu-id="45d81-108">Um valor **HRESULT** consiste nos seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="45d81-108">An **HRESULT** value consists of the following fields:</span></span> 
  
- <span data-ttu-id="45d81-109">Um código de 1 bit que indica severidade, onde zero representa êxito e 1 representa falha.</span><span class="sxs-lookup"><span data-stu-id="45d81-109">A 1-bit code indicating severity, where zero represents success and 1 represents failure.</span></span>
    
- <span data-ttu-id="45d81-110">Um valor reservado de 4 bits.</span><span class="sxs-lookup"><span data-stu-id="45d81-110">A 4-bit reserved value.</span></span>
    
- <span data-ttu-id="45d81-111">Um código de 11 bits indicando a responsabilidade pelo erro ou aviso, também conhecido como código de facilidade.</span><span class="sxs-lookup"><span data-stu-id="45d81-111">An 11-bit code indicating responsibility for the error or warning, also known as a facility code.</span></span>
    
- <span data-ttu-id="45d81-112">Um código de 16 bits descrevendo o erro ou aviso.</span><span class="sxs-lookup"><span data-stu-id="45d81-112">A 16-bit code describing the error or warning.</span></span>
    
<span data-ttu-id="45d81-113">A maioria dos métodos e funções de interface MAPI retornam valores **HRESULT** para fornecer uma formação de causa detalhada.</span><span class="sxs-lookup"><span data-stu-id="45d81-113">Most MAPI interface methods and functions return **HRESULT** values to provide detailed cause formation.</span></span> <span data-ttu-id="45d81-114">Os valores **HRESULT** também são usados amplamente nos métodos de interface OLE.</span><span class="sxs-lookup"><span data-stu-id="45d81-114">**HRESULT** values are also used widely in OLE interface methods.</span></span> <span data-ttu-id="45d81-115">O OLE fornece várias macros para conversão entre valores **HRESULT** e valores **SCODE** , outro tipo de dados comum para tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="45d81-115">OLE provides several macros for converting between **HRESULT** values and **SCODE** values, another common data type for error handling.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="45d81-116">No MAPI de 64 bits, **HRESULT** ainda é um valor de bit 32.</span><span class="sxs-lookup"><span data-stu-id="45d81-116">In 64-bit MAPI, **HRESULT** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="45d81-117">Para obter informações sobre o uso de OLE dos valores **HRESULT** , consulte a *referência do programador de OLE* .</span><span class="sxs-lookup"><span data-stu-id="45d81-117">For information about the OLE use of **HRESULT** values, see the  *OLE Programmer's Reference*  .</span></span> <span data-ttu-id="45d81-118">Para obter mais informações sobre o uso desses valores no MAPI, consulte [tratamento de erros](error-handling-in-mapi.md) e qualquer um dos seguintes métodos de interface:</span><span class="sxs-lookup"><span data-stu-id="45d81-118">For more information about the use of these values in MAPI, see [Error Handling](error-handling-in-mapi.md) and any of the following interface methods:</span></span> 
  
[<span data-ttu-id="45d81-119">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="45d81-119">IABLogon::GetLastError</span></span>](iablogon-getlasterror.md)
  
[<span data-ttu-id="45d81-120">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="45d81-120">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="45d81-121">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="45d81-121">IMAPIControl::GetLastError</span></span>](imapicontrol-getlasterror.md)
  
[<span data-ttu-id="45d81-122">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="45d81-122">IMAPITable::GetLastError</span></span>](imapitable-getlasterror.md)
  
[<span data-ttu-id="45d81-123">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="45d81-123">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="45d81-124">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="45d81-124">IMAPIViewAdviseSink::OnPrint</span></span>](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a><span data-ttu-id="45d81-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="45d81-125">See also</span></span>



[<span data-ttu-id="45d81-126">SCODE</span><span class="sxs-lookup"><span data-stu-id="45d81-126">SCODE</span></span>](scode.md)


[<span data-ttu-id="45d81-127">Tipos de dados MAPI</span><span class="sxs-lookup"><span data-stu-id="45d81-127">MAPI Data Types</span></span>](mapi-data-types.md)

