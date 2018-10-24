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
ms.openlocfilehash: 4687b07c89d866acbe3b6a8f4cde3262657a06b5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584244"
---
# <a name="declaring-form-interfaces"></a>Declarar interfaces de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Você pode simplificar as declarações de suas implementações das interfaces do formulário MAPI usando macros _interface__METHOD MAPI_, _onde é uma interface de formulário definida no arquivo de cabeçalho Mapiform.h_ . Não é necessário usar essas macros, mas se você não fizer isso, você deve tomar cuidado específico que suas declarações estão de acordo com as declarações no arquivo de cabeçalho Mapiform.h. Por exemplo, você poderia declarar a classe de objeto do formulário do seu servidor de forma semelhante ao seguinte: 
  
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



[Escrevendo códigos de servidor do formulário](writing-form-server-code.md)

