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
ms.openlocfilehash: 607105bd58a14a3510f1ae71246069440a4f05cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326191"
---
# <a name="openimsgsession"></a>OpenIMsgSession

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria e abre uma sessão de mensagem que agrupa as mensagens criadas nele. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |IMessage. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a>Parâmetros

 _lpMalloc_
  
> no Ponteiro para um objeto de alocador de memória expondo a interface [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) do OLE. O MAPI precisa usar esse método de alocação ao trabalhar com a interface [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) do OLE. 
    
 _ulFlags_
  
> no Serve deve ser zero. 
    
 _lppMsgSess_
  
> bota Ponteiro para um ponteiro para o objeto de sessão Message retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A sessão foi aberta.
    
MAPI_E_INVALID_PARAMETER
  
>  _lpMalloc_ ou _lppMsgSess_ é nulo. 
    
MAPI_E_INVALID_FLAGS
  
> Foram passados sinalizadores inVálidos.
    
MAPI_UNICODE
  
> Ao chamar essa função, um cliente ou um provedor de serviços define o sinalizador MAPI_UNICODE para criar arquivos Unicode. msg. O arquivo [IMessage](imessageimapiprop.md) resultante mostra STORE_UNICODE_OK em seu PR_STORE_SUPPORT_MASK e oferece suporte a Propriedades Unicode. 
    
## <a name="remarks"></a>Comentários

Uma sessão de mensagem é usada por aplicativos cliente e provedores de serviços que desejam lidar com vários objetos MAPI [IMessage: IMAPIProp](imessageimapiprop.md) relacionados à parte superior dos objetos OLE **IStorage** subjacentes. O cliente ou provedor usa as funções **OpenIMsgSession** e [CloseIMsgSession](closeimsgsession.md) para quebrar a criação dessas mensagens dentro de uma sessão de mensagem. Depois que a sessão de mensagem é aberta, o cliente ou o provedor passa um ponteiro para ele em uma chamada para [OpenIMsgOnIStg](openimsgonistg.md) para criar um novo objeto **IMessage**-on- **IStorage** . 
  
Uma sessão de mensagem mantém o controle de todos os objetos **IMessage**-on- **IStorage** criados durante a duração da sessão, além de todos os anexos e outras propriedades das mensagens. Quando um cliente ou provedor chama **CloseIMsgSession**, ele fecha todos esses objetos. Chamar **CloseIMsgSession** é a única maneira de fechar os objetos **IMessage**-on- **IStorage** . 
  
 O **OpenIMsgSession** é usado por clientes e provedores que exigem a capacidade de lidar com várias mensagens relacionadas como objetos do OLE **IStorage** . Se apenas uma dessas mensagens for aberta por vez, não será necessário controlar várias mensagens e nenhum motivo para criar uma sessão de mensagem com o **OpenIMsgSession**. 
  
Como está lidando com um objeto OLE subjacente, o MAPI precisa usar a alocação de memória OLE. Para obter mais informações sobre objetos de armazenamento estruturados OLE e alocação de memória OLE, consulte [OLE e transferência de dados](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  

