---
title: IMsgServiceAdminGetMsgServiceTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetMsgServiceTable
api_type:
- COM
ms.assetid: 064dd5ca-0108-4045-b17b-0bb29cb93346
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fcaebb96d4dca4e6bfbee7491dabeafcbd93a2eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410473"
---
# <a name="imsgserviceadmingetmsgservicetable"></a>IMsgServiceAdmin::GetMsgServiceTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à tabela de serviço de mensagens, uma lista dos serviços de mensagens no perfil.
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Sempre nulo.
    
 _lppTable_
  
> bota Um ponteiro para um ponteiro para a tabela de serviço de mensagens.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela de serviço de mensagens foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin:: GetMsgServiceTable** fornece acesso à tabela de serviço de mensagens, uma tabela que o MAPI mantém que lista os serviços de mensagens atualmente instalados no perfil da sessão. Para obter uma lista completa das colunas na tabela do serviço de mensagens, consulte [Message Service Table](message-service-tables.md).
  
A tabela de serviço de mensagens é estática. Depois que um cliente recebeu acesso a ele, as adições ou exclusões do serviço de mensagens subsequentes não o afetarão. Se não houver nenhum serviço de mensagens no perfil atual, **GetMsgServiceTable** retornará uma tabela com zero linhas. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MsgServiceTableDlg. cpp  <br/> |CMsgServiceTableDlg:: OnRefreshView  <br/> |MFCMAPI usa o método **IMsgServiceAdmin:: GetMsgServiceTable** para carregar o índice de serviços em um perfil para renderizar no modo de exibição.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

