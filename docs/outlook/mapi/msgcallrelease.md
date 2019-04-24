---
title: MSGCALLRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGCALLRELEASE
api_type:
- COM
ms.assetid: 23c08597-41f0-4f48-a63e-79962fa812bc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9ffaab1e9cc381be2abfb389f4b72067dca2438b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338560"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma função de retorno de chamada que pode liberar uma interface **IStorage** após a versão final de um objeto **IMessage** criado com a função [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |IMessage. h  <br/> |
|Função definida implementada por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
|Função definida chamada por:  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>Parâmetros

 _ulCallerData_
  
> no Contém informações de aplicativo de chamada sobre a interface **IMessage** . 
    
 _lpMessage_
  
> no Ponteiro para a mensagem e os anexos de nível superior que foram liberados.
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  

