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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342137"
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
  
> [in] **true** para incrementar a contagem de bloqueio; caso contrário, **false**.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam o **método IMAPIFormFactory::LockServer** para manter um aplicativo de servidor de formulário aberto na memória. Manter o servidor de formulários na memória melhora seu desempenho quando os formulários são criados e liberados com frequência. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

O **método IMAPIFormFactory::LockServer** é muito semelhante ao [método IClassFactory::LockServer.](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) Essencialmente, o **método IMAPIFormFactory::LockServer** mantém uma contagem de quantas vezes ele foi chamado; desde que essa contagem seja maior que 0, o método impede que o servidor de formulário seja descarregado da memória. Você pode usar a [função CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) para implementar isso. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

