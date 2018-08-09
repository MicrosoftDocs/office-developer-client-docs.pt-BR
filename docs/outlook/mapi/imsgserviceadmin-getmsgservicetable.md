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
ms.openlocfilehash: 588a32cb2a468c84dfc513af5e4abf6a9a1d0286
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767516"
---
# <a name="imsgserviceadmingetmsgservicetable"></a>IMsgServiceAdmin::GetMsgServiceTable

  
  
**Aplica-se a**: Outlook 
  
Fornece acesso à tabela de serviço de mensagem, uma lista dos serviços de mensagem no perfil.
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Sempre nulo.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela de serviços de mensagem.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A tabela de serviços de mensagem foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin::GetMsgServiceTable** fornece acesso à tabela de serviço de mensagem, uma tabela que mantém MAPI que lista os serviços de mensagem instalados atualmente no perfil da sessão. Para obter uma lista completa das colunas na tabela de serviço de mensagens, consulte a [Tabela de serviços de mensagem](message-service-tables.md).
  
A tabela de serviços de mensagem é estática. Depois que um cliente tem acesso a ele, adições de serviço de mensagem subsequente ou exclusões não afetará-lo. Se não houver nenhuma mensagem serviços no perfil atual, **GetMsgServiceTable** retorna uma tabela com zero linhas. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnRefreshView  <br/> |MFCMAPI usa o método **IMsgServiceAdmin::GetMsgServiceTable** para carregar a tabela de serviços em um perfil para renderizar no modo de exibição.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

