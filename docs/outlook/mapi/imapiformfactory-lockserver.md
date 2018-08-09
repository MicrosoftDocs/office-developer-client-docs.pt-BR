---
title: IMAPIFormFactoryLockServer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.LockServer
api_type:
- COM
ms.assetid: b9bd389a-6975-41a2-a2f4-e501312e434b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c33fea8a2aba875fcdc06dea3343add4b7ac5dde
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767014"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**Aplica-se a**: Outlook 
  
Mantém um servidor de formulário aberto na memória.
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _fLockServer_
  
> [in] **true** para incrementar a contagem de bloqueio; Caso contrário, **false**.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método de **IMAPIFormFactory::LockServer** para manter um aplicativo de servidor do formulário aberto na memória. Manter o servidor de formulário na memória melhora o seu desempenho quando formulários frequentemente são criados e lançados. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

O método **IMAPIFormFactory::LockServer** é muito semelhante ao método [IClassFactory::LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) . Basicamente, o método **IMAPIFormFactory::LockServer** mantém uma contagem de quantas vezes ele tiver sido chamada; desde que essa contagem for maior que 0, o método impede que o servidor do formulário está sendo descarregado da memória. Você pode usar a função [CoLockObjectExternal](http://msdn.microsoft.com/en-us/library/ms680592%28VS.85%29.aspx) para implementar isso. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

