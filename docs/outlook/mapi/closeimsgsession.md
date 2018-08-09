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
ms.openlocfilehash: c190691c8cfcb9b049bcf9ee4f21436e20955def
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766282"
---
# <a name="closeimsgsession"></a>CloseIMsgSession

  
  
**Aplica-se a**: Outlook 
  
Fecha uma sessão de mensagem e todas as mensagens criadas dentro dessa sessão. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |IMessage.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a>Parâmetros

 _lpMsgSess_
  
> [in] Ponteiro para o objeto de sessão de mensagem obtido com a função [OpenIMsgSession](openimsgsession.md) no início da sessão de mensagem. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Uma sessão de mensagens é usada por aplicativos cliente e provedores de serviços que deseja lidar com vários objetos relacionados de MAPI **IMessage** construídos sobre objetos OLE **IStorage** subjacentes. O cliente ou o provedor usa as funções [OpenIMsgSession](openimsgsession.md) e **CloseIMsgSession** para quebrar a criação dessas mensagens de uma sessão de mensagens. Depois que a sessão de mensagens é aberta, o cliente ou o provedor passa um ponteiro para ele em uma chamada para [OpenIMsgOnIStg](openimsgonistg.md) para criar um novo **IMessage**- on - objeto **|** . 
  
Uma sessão de mensagens rastreia de todos os objetos de **IMessage**- on - **IStorage** abertos durante a duração da sessão, além de todos os anexos e outras propriedades das mensagens. Quando um cliente ou provedor chama **CloseIMsgSession**, ele fecha todos esses objetos. Chamar o **CloseIMsgSession** é a única maneira de fechar **IMessage**- on - **IStorage** objetos. 
  

