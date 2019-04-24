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
# <a name="declaring-form-interfaces"></a>Declarar interfaces de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Você pode simplificar as declarações de suas implementações de interfaces de formulário MAPI usando as macros do MAPI_ _interface__METHOD, onde _interface_ é uma interface de formulário definida no arquivo de cabeçalho Mapiform. h. Não é necessário usar essas macros, mas se você não fizer isso, deverá ter um cuidado especial de que suas declarações estão de acordo com as declarações no arquivo de cabeçalho Mapiform. h. Por exemplo, você poderia declarar a classe de objeto Form do seu servidor de formulário como o seguinte: 
  
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

## <a name="see-also"></a>Confira também



[Gravando código de servidor de formulário](writing-form-server-code.md)

