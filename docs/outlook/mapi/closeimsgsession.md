---
title: CloseIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CloseIMsgSession
api_type:
- COM
ms.assetid: a0a17309-fc59-4822-be9b-b6f623b68bb1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 877bebf0a156c99907505d815ca8d36a4b398678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412034"
---
# <a name="closeimsgsession"></a>CloseIMsgSession

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fecha uma sessão de mensagem e todas as mensagens criadas nessa sessão. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |IMessage. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a>Parâmetros

 _lpMsgSess_
  
> no Ponteiro para o objeto de sessão de mensagem obtido usando a função [OpenIMsgSession](openimsgsession.md) no início da sessão de mensagem. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Uma sessão de mensagem é usada por aplicativos cliente e provedores de serviços que desejam lidar com vários objetos MAPI **IMessage** relacionados criados na parte superior dos objetos OLE **IStorage** subjacentes. O cliente ou provedor usa as funções [OpenIMsgSession](openimsgsession.md) e **CloseIMsgSession** para quebrar a criação dessas mensagens dentro de uma sessão de mensagem. Depois que a sessão de mensagem é aberta, o cliente ou o provedor passa um ponteiro para ele em uma chamada para [OpenIMsgOnIStg](openimsgonistg.md) para criar um novo objeto **IMessage**-on- **IStorage** . 
  
Uma sessão de mensagem mantém o controle de todos os objetos **IMessage**-on- **IStorage** abertos durante a duração da sessão, além de todos os anexos e outras propriedades das mensagens. Quando um cliente ou provedor chama **CloseIMsgSession**, ele fecha todos esses objetos. Chamar **CloseIMsgSession** é a única maneira de fechar os objetos **IMessage**-on- **IStorage** . 
  

