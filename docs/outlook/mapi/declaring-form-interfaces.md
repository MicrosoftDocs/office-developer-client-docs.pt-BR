---
title: Declarar interfaces de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0fa742b7ff6d98e3a0f475accbc440d22eac0919
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337055"
---
# <a name="declaring-form-interfaces"></a><span data-ttu-id="3866d-103">Declarar interfaces de formulário</span><span class="sxs-lookup"><span data-stu-id="3866d-103">Declaring Form Interfaces</span></span>

  
  
<span data-ttu-id="3866d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3866d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3866d-105">Você pode simplificar as declarações de suas implementações de interfaces de formulário MAPI usando as macros do MAPI_ _interface__METHOD, onde _interface_ é uma interface de formulário definida no arquivo de cabeçalho Mapiform. h.</span><span class="sxs-lookup"><span data-stu-id="3866d-105">You can simplify the declarations of your implementations of MAPI form interfaces by using the MAPI_ _interface__METHOD macros, where  _interface_ is a form interface defined in the Mapiform.h header file.</span></span> <span data-ttu-id="3866d-106">Não é necessário usar essas macros, mas se você não fizer isso, deverá ter um cuidado especial de que suas declarações estão de acordo com as declarações no arquivo de cabeçalho Mapiform. h.</span><span class="sxs-lookup"><span data-stu-id="3866d-106">You are not required to use these macros, but if you do not, you should take particular care that your declarations conform to the declarations in the Mapiform.h header file.</span></span> <span data-ttu-id="3866d-107">Por exemplo, você poderia declarar a classe de objeto Form do seu servidor de formulário como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3866d-107">For example, you could declare your form server's form object class like the following:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="3866d-108">Confira também</span><span class="sxs-lookup"><span data-stu-id="3866d-108">See also</span></span>



[<span data-ttu-id="3866d-109">Gravando código de servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="3866d-109">Writing Form Server Code</span></span>](writing-form-server-code.md)

