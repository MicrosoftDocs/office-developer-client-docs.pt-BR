---
title: Declarando interfaces de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0fa742b7ff6d98e3a0f475accbc440d22eac0919
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437508"
---
# <a name="declaring-form-interfaces"></a>Declarando interfaces de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Você pode simplificar as declarações de suas implementações de interfaces de formulário MAPI usando as macros MAPI_ _interface__METHOD, onde interface é uma  _interface_ de formulário definida no arquivo de header Mapiform.h. Não é necessário usar essas macros, mas se não usar, tome cuidado particular com as declarações que estão em conformidade com as declarações no arquivo de header Mapiform.h. For example, you could declare your form server's form object class like the following: 
  
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



[Escrevendo código do servidor de formulário](writing-form-server-code.md)

