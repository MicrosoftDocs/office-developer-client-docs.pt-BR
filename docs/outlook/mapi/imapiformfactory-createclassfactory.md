---
title: IMAPIFormFactoryCreateClassFactory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.CreateClassFactory
api_type:
- COM
ms.assetid: dceb21b1-be5e-418d-b0c9-db39195fc82e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 823e10a1f496f5f5e8bab00f94d700d06e753b48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767039"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**Aplica-se a**: Outlook 
  
Retorna um objeto de fábrica de classe do formulário.
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>Parâmetros

 _clsidForm_
  
> [in] Um identificador de classe do formulário a ser criado pela fábrica de classe.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lppClassFactory_
  
> [out] Um ponteiro para o objeto de classe de fábrica.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O objeto de classe de fábrica foi retornado.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método de **IMAPIFormFactory::CreateClassFactory** para obter um alocador de classe de um formulário específico. O alocador de classe é usado para criar instâncias de um formulário que processa mensagens de uma classe específica e controlar o acesso a essas instâncias. 
  
O método **CreateClassFactory** é chamado pelo visualizadores de formulário para obter um objeto de fábrica de classe para servidores de formulário que implementar várias classes de mensagem. Esse método recebe um identificador de classe (CLSID) como um parâmetro. Com base no parâmetro, esse método pode determinar o tipo específico de objeto de fábrica de classe para retornar. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Você pode retornar da sua implementação **CreateClassFactory** o mesmo objeto de fábrica de classe em várias chamadas para o mesmo identificador de classe. Criando uma nova instância de fábrica de classe não é necessária. 
  
Você pode ter uma implementação de fábrica de classe única que cria instâncias de fábrica de classe apropriado sob demanda ou várias implementações de fábrica de classe, uma para cada classe de mensagem.
  
## <a name="see-also"></a>Confira também



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

