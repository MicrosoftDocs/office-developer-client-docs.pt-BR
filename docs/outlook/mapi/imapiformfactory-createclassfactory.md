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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416073"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um objeto de fábrica de classe para o formulário.
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>Parâmetros

 _clsidForm_
  
> [in] Um identificador de classe para o formulário a ser criado pela fábrica de classe.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lppClassFactory_
  
> [out] Um ponteiro para o objeto de fábrica de classe.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O objeto de fábrica de classe foi retornado.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam **o método IMAPIFormFactory::CreateClassFactory** para obter um fábrica de classe para um formulário específico. A fábrica de classe é usada para criar instâncias de um formulário que lida com mensagens de uma classe específica e para controlar o acesso a essas instâncias. 
  
O **método CreateClassFactory** é chamado pelos visualizadores de formulário para obter um objeto de fábrica de classe para servidores de formulário que implementam várias classes de mensagens. Esse método recebe um identificador de classe (CLSID) como um parâmetro. Com base nesse parâmetro, esse método pode determinar o tipo específico de objeto de fábrica de classe a ser retornada. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Você pode retornar da implementação **de CreateClassFactory** o mesmo objeto de fábrica de classe em várias chamadas para o mesmo identificador de classe. Não é necessário criar uma nova instância de fábrica de classe. 
  
Você pode ter uma implementação de fábrica de classe única que crie instâncias de fábrica de classe apropriadas sob demanda ou várias implementações de fábrica de classe, uma para cada classe de mensagem.
  
## <a name="see-also"></a>Confira também



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

