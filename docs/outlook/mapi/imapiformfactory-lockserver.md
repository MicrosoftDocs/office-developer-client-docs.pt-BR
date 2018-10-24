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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ab51b939651bc3c121f357545969d26832a19d19
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389050"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método de **IMAPIFormFactory::LockServer** para manter um aplicativo de servidor do formulário aberto na memória. Manter o servidor de formulário na memória melhora o seu desempenho quando formulários frequentemente são criados e lançados. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

O método **IMAPIFormFactory::LockServer** é muito semelhante ao método [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) . Basicamente, o método **IMAPIFormFactory::LockServer** mantém uma contagem de quantas vezes ele tiver sido chamada; desde que essa contagem for maior que 0, o método impede que o servidor do formulário está sendo descarregado da memória. Você pode usar a função [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) para implementar isso. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

