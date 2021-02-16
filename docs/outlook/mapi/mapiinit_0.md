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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357292"
---
# <a name="mapiinit_0"></a>MAPIINIT_0

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Transmite opções para a [função MAPIInitialize.](mapiinitialize.md) 
  
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
  
> Um valor inteiro que representa o número de versão do **MAPIINIT_0** estrutura. O **membro ulVersion** é para expansão futura e não representa a versão da interface MAPI. Atualmente, **ulVersion** deve ser definido como MAPI_INIT_VERSION. 
    
 **ulFlags**
  
> A máscara de bits de sinalizadores usada para controlar a inicialização da sessão MAPI. Os sinalizadores a seguir podem ser definidos:
    
MAPI_MULTITHREAD_NOTIFICATIONS 
  
> MAPI should generate notifications using a thread dedicated to notification handling instead of the first thread used to call **MAPIInitialize**.
    
MAPI_NT_SERVICE 
  
> O chamador está sendo executado como um serviço do Windows. Os chamadores que não estão sendo executados como um serviço do Windows não devem definir esse sinalizador; os chamadores que estão sendo executados como um serviço devem definir esse sinalizador.
    
MAPI_NO_COINIT
  
> De definida MAPI_NO_COINT sinalizador para que **MAPIInitialize** não tente inicializar COM com uma chamada para [CoInitialize](https://msdn.microsoft.com/library/0f171cf4-87b9-43a6-97f2-80ed344fe376%28Office.15%29.aspx). Se uma estrutura **MAPIINIT_0** for passada para **MAPIInitialize** com  _ulFlags_ definido como MAPI_NO_COINIT, o MAPI assumirá que COM já foi inicializado e ignorará a chamada para **CoInitialize**.
    
## <a name="remarks"></a>Comentários

Clientes multithreaded devem definir o sinalizador MAPI_MULTITHREAD_NOTIFICATIONS leitura. Se o sinalizador não estiver definido, as notificações serão geradas no thread usado para fazer a primeira chamada para **MAPIInitialize**. 
  
Para obter mais informações sobre quando definir esse sinalizador e como implementar a segurança de thread em um cliente, consulte [Threading em MAPI](threading-in-mapi.md). 
  
## <a name="see-also"></a>Confira também



[MAPIInitialize](mapiinitialize.md)


[Estruturas MAPI](mapi-structures.md)

