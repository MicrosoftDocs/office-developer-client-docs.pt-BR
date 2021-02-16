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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405909"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma função de retorno de chamada que pode liberar uma interface **IStorage** após o lançamento final de um objeto **IMessage** criado sobre ele com a função [OpenIMsgOnIStg.](openimsgonistg.md) 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Imessage.h  <br/> |
|Função definida implementada por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
|Função definida chamada por:  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>Parâmetros

 _ulCallerData_
  
> [in] Contém informações de aplicativo de chamada sobre a interface **IMessage.** 
    
 _lpMessage_
  
> [in] Ponteiro para a mensagem de nível superior e anexos que foram liberados.
    
## <a name="return-value"></a>Valor retornado

Nenhum
  

