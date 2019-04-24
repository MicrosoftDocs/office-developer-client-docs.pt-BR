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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6e616a76d9665b602184e88566384506fcce5697
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342172"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um objeto Factory de classe para o formulário.
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>Parâmetros

 _clsidForm_
  
> no Um identificador de classe para o formulário a ser criado pela fábrica de classes.
    
 _ulFlags_
  
> no Serve deve ser zero.
    
 _lppClassFactory_
  
> bota Um ponteiro para o objeto Factory de classe.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O objeto Factory de classe foi retornado.
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIFormFactory:: CreateClassFactory** para obter um alocador de classe para um formulário específico. A fábrica de classes é usada para criar instâncias de um formulário que manipula mensagens de uma classe específica e para controlar o acesso a essas instâncias. 
  
O método **CreateClassFactory** é chamado por visualizadores de formulários para obter um objeto Factory de classe para servidores de formulário que implementam várias classes de mensagens. Este método recebe um identificador de classe (CLSID) como um parâmetro. Com base nesse parâmetro, este método pode determinar o tipo de objeto de fábrica de classe específico a ser retornado. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Você pode retornar da implementação do **CreateClassFactory** o mesmo objeto de fábrica de classe em várias chamadas para o mesmo identificador de classe. Não é necessário criar uma nova instância de fábrica de classes. 
  
Você pode ter uma implementação de fábrica de classe única que cria instâncias de fábrica de classe apropriadas sob demanda ou várias implementações de fábrica de classes, uma para cada classe de mensagem.
  
## <a name="see-also"></a>Confira também



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

