---
title: SCODE
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
ms.assetid: 2348cce1-07c3-49ed-ae03-79e477d3c6c2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6cd9dfe8fabd1ae7a4389550c628fb7ceff09ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770319"
---
# <a name="scode"></a><span data-ttu-id="7e1c2-103">SCODE</span><span class="sxs-lookup"><span data-stu-id="7e1c2-103">SCODE</span></span>

<span data-ttu-id="7e1c2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7e1c2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7e1c2-105">Um valor de status de 32 bits que é usado para descrever um erro ou aviso.</span><span class="sxs-lookup"><span data-stu-id="7e1c2-105">A 32-bit status value that is used to describe an error or warning.</span></span> 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a><span data-ttu-id="7e1c2-106">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="7e1c2-106">Remarks</span></span>

<span data-ttu-id="7e1c2-107">O tipo de dados **SCODE** é o mesmo que o tipo de dados [HRESULT](hresult.md) .</span><span class="sxs-lookup"><span data-stu-id="7e1c2-107">The **SCODE** data type is the same as the [HRESULT](hresult.md) data type.</span></span> 
  
<span data-ttu-id="7e1c2-108">Um valor **SCODE** é dividido em quatro campos:</span><span class="sxs-lookup"><span data-stu-id="7e1c2-108">An **SCODE** value is divided into four fields:</span></span> 
  
- <span data-ttu-id="7e1c2-109">Um código de gravidade bit único que é definido como 0 para indicar êxito e 1 para indicar falha.</span><span class="sxs-lookup"><span data-stu-id="7e1c2-109">A single-bit severity code which is set to 0 to indicate success and 1 to indicate failure.</span></span>
    
- <span data-ttu-id="7e1c2-110">Um campo reservado de 11 bits</span><span class="sxs-lookup"><span data-stu-id="7e1c2-110">An 11-bit reserved field</span></span>
    
- <span data-ttu-id="7e1c2-111">Um código de instalações de 4 bits que indica a área responsável pelo erro ou aviso.</span><span class="sxs-lookup"><span data-stu-id="7e1c2-111">A 4-bit facility code which indicates the area responsible for the error or warning.</span></span>
    
- <span data-ttu-id="7e1c2-112">Um erro de 16 bits ou código de aviso que descreve o problema que está causando o erro ou aviso.</span><span class="sxs-lookup"><span data-stu-id="7e1c2-112">A 16-bit error or warning code which describes the problem that is causing the error or warning.</span></span>
    
<span data-ttu-id="7e1c2-113">Muitas das funções MAPI e métodos retornam valores **SCODE** definidos como tipos de dados **HRESULT** , assim como as funções e os métodos OLE.</span><span class="sxs-lookup"><span data-stu-id="7e1c2-113">Many of the MAPI functions and methods return **SCODE** values defined as **HRESULT** data types as do the OLE methods and functions.</span></span> <span data-ttu-id="7e1c2-114">OLE define várias macros que podem ser usadas para converter entre um **SCODE** e um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7e1c2-114">OLE defines several macros that can be used to convert between an **SCODE** and an **HRESULT**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7e1c2-115">Em MAPI de 64 bits, **SCODE** ainda é um valor de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7e1c2-115">In 64-bit MAPI, **SCODE** is still a 32-bit value.</span></span> 
  
<span data-ttu-id="7e1c2-116">Para obter mais informações sobre como o MAPI usa o tipo de dados **SCODE** , consulte o [Tratamento de erros](error-handling-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="7e1c2-116">For more information about how MAPI uses the **SCODE** data type, see [Error Handling](error-handling-in-mapi.md).</span></span> <span data-ttu-id="7e1c2-117">Para obter mais informações sobre o OLE e o tipo de dados **SCODE** , consulte a *referência do programador do OLE* .</span><span class="sxs-lookup"><span data-stu-id="7e1c2-117">For more information about OLE and the **SCODE** data type, see the  *OLE Programmer's Reference*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7e1c2-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e1c2-118">See also</span></span>



[<span data-ttu-id="7e1c2-119">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7e1c2-119">HRESULT</span></span>](hresult.md)


[<span data-ttu-id="7e1c2-120">Tipos de dados MAPI</span><span class="sxs-lookup"><span data-stu-id="7e1c2-120">MAPI Data Types</span></span>](mapi-data-types.md)

