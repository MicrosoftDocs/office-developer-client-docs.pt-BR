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
ms.openlocfilehash: cb5cb5a0169e716f7fcc7f596660bc0222c51c84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572155"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

