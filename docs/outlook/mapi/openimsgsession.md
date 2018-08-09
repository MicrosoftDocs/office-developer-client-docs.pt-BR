---
title: OpenIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenIMsgSession
api_type:
- COM
ms.assetid: f75229e3-5f44-4298-8706-9eddf0ef124c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e7f652e7426792d8b4c878b7f6738439aec65348
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768173"
---
# <a name="openimsgsession"></a>OpenIMsgSession

  
  
**Aplica-se a**: Outlook 
  
Cria e abre uma sessão de mensagem que agrupa as mensagens criadas com ela. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |IMessage.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a>Parâmetros

 _lpMalloc_
  
> [in] Ponteiro para um objeto de alocador de memória expondo a interface OLE [IMalloc](http://msdn.microsoft.com/library/047f281e-2665-4d6d-9a0b-918cd3339447%28Office.15%29.aspx) . MAPI deve usar esse método de alocação ao trabalhar com a interface OLE [IStorage](http://msdn.microsoft.com/library/stg.istorage%28Office.15%29.aspx) . 
    
 _ulFlags_
  
> [in] Reservado; deve ser zero. 
    
 _lppMsgSess_
  
> [out] Ponteiro para um ponteiro para o objeto de sessão de mensagem retornada.
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> A sessão foi aberta.
    
MAPI_E_INVALID_PARAMETER
  
>  _lpMalloc_ ou _lppMsgSess_ é nulo. 
    
MAPI_E_INVALID_FLAGS
  
> Sinalizadores inválidos foram passados.
    
MAPI_UNICODE
  
> Ao chamar essa função, um cliente ou serviço provedor define o sinalizador MAPI_UNICODE para criar os arquivos do. msg Unicode. O arquivo resultante de [Imessage](imessageimapiprop.md) mostra STORE_UNICODE_OK no seu PR_STORE_SUPPORT_MASK e oferece suporte a Unicode propriedades. 
    
## <a name="remarks"></a>Comentários

Uma sessão de mensagens é usada pelos aplicativos cliente e provedores de serviço que deseja lidar com vários relacionados MAPI [IMessage: IMAPIProp](imessageimapiprop.md) objetos construídos sobre objetos OLE **IStorage** subjacentes. O cliente ou o provedor usa as funções **OpenIMsgSession** e [CloseIMsgSession](closeimsgsession.md) para quebrar a criação dessas mensagens de uma sessão de mensagens. Depois que a sessão de mensagens é aberta, o cliente ou o provedor passa um ponteiro para ele em uma chamada para [OpenIMsgOnIStg](openimsgonistg.md) para criar um novo **IMessage**- on - objeto **|** . 
  
Uma sessão de mensagens rastreia de todos os **IMessage**- on - objetos **IStorage** criados durante a duração da sessão, além de todos os anexos e outras propriedades das mensagens. Quando um cliente ou provedor chama **CloseIMsgSession**, ele fecha todos esses objetos. Chamar o **CloseIMsgSession** é a única maneira de fechar **IMessage**- on - **IStorage** objetos. 
  
 **OpenIMsgSession** é usado por clientes e provedores que requerem a capacidade de lidar com várias mensagens relacionadas como objetos OLE **IStorage** . Se houver apenas uma dessas mensagens para ser aberto por vez, não há nenhuma necessidade para controlar várias mensagens e não há motivo para criar uma sessão de mensagem com **OpenIMsgSession**. 
  
Porque ele está lidando com um objeto OLE subjacente, MAPI deve usar a alocação de memória do OLE. Para obter mais informações sobre objetos de armazenamento estruturado OLE e alocação de memória do OLE, consulte [OLE e transferência de dados](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  

