---
title: MAPIINIT_0
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIINIT_0
api_type:
- COM
ms.assetid: 70739711-ff43-407d-bc8b-6baf7a476fef
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: de31fe7d472b143ed8f3c108dca84a019b5ce103
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391147"
---
# <a name="mapiinit0"></a>MAPIINIT_0

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Transmite opções para a função [MAPIInitialize](mapiinitialize.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIX. H  <br/> |
   
```cpp
typedef struct
{
  ULONG ulVersion;
  ULONG ulFlags;
} MAPIINIT_0, FAR *LPMAPIINIT_0;

```

## <a name="members"></a>Members

 **ulVersion**
  
> Um valor inteiro que representa o número de versão da estrutura **MAPIINIT_0** . O membro **ulVersion** é para expansão futura e não representam a versão da interface do MAPI. Atualmente, **ulVersion** deve ser definida como MAPI_INIT_VERSION. 
    
 **ulFlags**
  
> A bitmask dos sinalizadores usados para controlar a inicialização da sessão MAPI. Sinalizadores a seguir podem ser definidos:
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI deve gerar notificações usando um thread dedicado a notificação manipulação em vez do primeiro segmento usado para chamar **MAPIInitialize**.
    
MAPI_NT_SERVICE 
  
> O chamador está sendo executado como um serviço do Windows. Chamadores que não estejam executando um serviço do Windows não deve definir esse sinalizador; os chamadores que estão sendo executados como um serviço devem definir esse sinalizador.
    
MAPI_NO_COINIT
  
> Defina o sinalizador MAPI_NO_COINT para que **MAPIInitialize** não tenta inicializar COM uma chamada a [CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx). Se uma estrutura **MAPIINIT_0** é passada para **MAPIInitialize** com _ulFlags_ definido como MAPI_NO_COINIT, MAPI partirá do pressuposto de que COM já foi inicializado e ignora a chamada para **CoInitialize**.
    
## <a name="remarks"></a>Comentários

Clientes multithreaded devem definir o sinalizador MAPI_MULTITHREAD_NOTIFICATIONS. Se o sinalizador não estiver definido, as notificações são geradas no thread usado para tornar a primeira chamada para **MAPIInitialize**. 
  
Para obter mais informações sobre quando definir esse sinalizador e como implementar a segurança do thread em um cliente, consulte [Threading in MAPI](threading-in-mapi.md). 
  
## <a name="see-also"></a>Confira também



[MAPIInitialize](mapiinitialize.md)


[Estruturas MAPI](mapi-structures.md)

