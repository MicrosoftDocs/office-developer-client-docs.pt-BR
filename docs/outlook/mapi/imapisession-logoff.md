---
title: IMAPISessionLogoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9dfc3b3381139b6b7fe47fb369d1cd69ee5e9677
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587835"
---
# <a name="imapisessionlogoff"></a>IMAPISession::Logoff

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Finaliza uma sessão MAPI.
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um identificador para a janela pai de todas as caixas de diálogo ou do windows a ser exibido. Esse parâmetro será ignorado se o sinalizador MAPI_LOGOFF_UI não estiver definido.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controlam a operação de logoff. Sinalizadores a seguir podem ser definidos:
    
MAPI_LOGOFF_SHARED 
  
> Se esta sessão é compartilhada, todos os clientes que feito logon usando a sessão compartilhada devem ser notificados de que o logoff em andamento. Os clientes devem fazer logoff. Qualquer cliente que está usando a sessão compartilhada pode definir esse sinalizador. MAPI_LOGOFF_SHARED será ignorada se a sessão atual não é compartilhada.
    
MAPI_LOGOFF_UI 
  
> **Fazer logoff** pode exibir uma caixa de diálogo durante a operação, possivelmente solicitando a confirmação do usuário. 
    
 _ulReserved_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A operação de logoff foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

O método **IMAPISession::Logoff** termina uma sessão MAPI. Quando o **Logoff** retorna, nenhum dos métodos, exceto [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) pode ser chamado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando o **Logoff** retorna, libere o objeto de sessão chamando seu método **IUnknown:: Release** . 
  
Para obter mais informações sobre como encerrar uma sessão, consulte [encerrar uma sessão MAPI](ending-a-mapi-session.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::Logoff  <br/> |MFCMAPI usa o método **IMAPISession::Logoff** fazer logoff da sessão antes de liberá-la.  <br/> |
   
> [!NOTE]
> Devido ao comportamento de desligamento rápido introduzido no Microsoft Office Outlook 2007 Service Pack 2, o Microsoft Outlook 2010 e o Microsoft Outlook 2013, clientes nunca devem passar o parâmetro **MAPI_LOGOFF_SHARED** para [IMAPISession::Logoff](imapisession-logoff.md). Passar **MAPI_LOGOFF_SHARED** fará com que todos os clientes MAPI começar o desligamento e ocorrerá um comportamento inesperado. 
  
## <a name="see-also"></a>Confira também



[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Finalizar uma sessão MAPI](ending-a-mapi-session.md)

