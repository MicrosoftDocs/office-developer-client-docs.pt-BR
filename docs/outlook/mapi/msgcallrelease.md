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
ms.openlocfilehash: aaa1adaa170349c3df3a2256802a502cb2512b20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768139"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**Aplica-se a**: Outlook 
  
Define uma função de retorno de chamada que pode liberar uma interface **IStorage** após o lançamento final de um objeto **IMessage** construído sobre ele com a função [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |IMessage.h  <br/> |
|Função definido implementada por:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
|Função definido chamada pelo:  <br/> |MAPI  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a>Parâmetros

 _ulCallerData_
  
> [in] Contém informações de aplicativo chamada sobre a interface **IMessage** . 
    
 _lpMessage_
  
> [in] Ponteiro para a mensagem de nível superior e os anexos que foram liberados.
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  

