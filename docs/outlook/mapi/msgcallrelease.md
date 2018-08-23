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
ms.openlocfilehash: e9a1c416cbf992c9cbcfb5de42d302ff16e7f521
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573184"
---
# <a name="msgcallrelease"></a>MSGCALLRELEASE

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  

