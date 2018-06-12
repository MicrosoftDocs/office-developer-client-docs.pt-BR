---
title: Declarando Interfaces de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8f4d8842efbba2f1f2b7281e5d4741b89f975b3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766372"
---
# <a name="declaring-form-interfaces"></a><span data-ttu-id="6bf2b-103">Declarando Interfaces de formulário</span><span class="sxs-lookup"><span data-stu-id="6bf2b-103">Declaring Form Interfaces</span></span>

  
  
<span data-ttu-id="6bf2b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6bf2b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6bf2b-105">Você pode simplificar as declarações de suas implementações das interfaces do formulário MAPI usando macros _interface__METHOD MAPI_, _onde é uma interface de formulário definida no arquivo de cabeçalho Mapiform.h_ .</span><span class="sxs-lookup"><span data-stu-id="6bf2b-105">You can simplify the declarations of your implementations of MAPI form interfaces by using the MAPI_ _interface__METHOD macros, where  _interface_ is a form interface defined in the Mapiform.h header file.</span></span> <span data-ttu-id="6bf2b-106">Não é necessário usar essas macros, mas se você não fizer isso, você deve tomar cuidado específico que suas declarações estão de acordo com as declarações no arquivo de cabeçalho Mapiform.h.</span><span class="sxs-lookup"><span data-stu-id="6bf2b-106">You are not required to use these macros, but if you do not, you should take particular care that your declarations conform to the declarations in the Mapiform.h header file.</span></span> <span data-ttu-id="6bf2b-107">Por exemplo, você poderia declarar a classe de objeto do formulário do seu servidor de forma semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="6bf2b-107">For example, you could declare your form server's form object class like the following:</span></span> 
  
```cpp
class CMyForm : public IPersistMessage, public IMAPIForm,
                public IMAPIFormAdviseSink
{
public:
    CMyForm(CClassFactory *);    // constructorr takes a class factory object
    ~CMyForm(void);
// MAPI methods that need to be implemented.
    MAPI_IUNKNOWN_METHODS(IMPL);
    MAPI_GETLASTERROR_METHOD(IMPL);
    MAPI_IPERSISTMESSAGE_METHODS(IMPL);
    MAPI_IMAPIFORM_METHODS(IMPL);
    MAPI_IMAPIFORMADVISESINK_METHODS(IMPL);
// Add other implementation specific items.
};

```

## <a name="see-also"></a><span data-ttu-id="6bf2b-108">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bf2b-108">See also</span></span>



[<span data-ttu-id="6bf2b-109">Escrevendo códigos de servidor do formulário</span><span class="sxs-lookup"><span data-stu-id="6bf2b-109">Writing Form Server Code</span></span>](writing-form-server-code.md)

