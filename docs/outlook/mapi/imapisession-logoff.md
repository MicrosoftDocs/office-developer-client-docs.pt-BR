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
ms.openlocfilehash: 317c3702415ddf30038ccd0d40cdf0f19abc61f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338105"
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
  
> no Uma alça para a janela pai de todas as caixas de diálogo ou janelas a serem exibidas. Esse parâmetro será ignorado se o sinalizador MAPI_LOGOFF_UI não estiver definido.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam a operação de logoff. Os seguintes sinalizadores podem ser definidos:
    
MAPI_LOGOFF_SHARED 
  
> Se esta sessão for compartilhada, todos os clientes que fizeram logon usando a sessão compartilhada devem ser notificados do logoff em andamento. Os clientes devem fazer logoff. Qualquer cliente que esteja usando a sessão compartilhada poderá definir esse sinalizador. MAPI_LOGOFF_SHARED será ignorada se a sessão atual não for compartilhada.
    
MAPI_LOGOFF_UI 
  
> O **logoff** pode exibir uma caixa de diálogo durante a operação, possivelmente solicitando a confirmação do usuário. 
    
 _ulReserved_
  
> no Serve deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de logoff foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

O método **IMAPISession:: logoff** encerra uma sessão MAPI. Quando o **logoff** retornar, nenhum dos métodos exceto [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) poderá ser chamado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando o **logoff** retornar, libere o objeto Session chamando seu método **IUnknown:: Release** . 
  
Para obter mais informações sobre como encerrar uma sessão, consulte [finalizar uma sessão MAPI](ending-a-mapi-session.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIObjects. cpp  <br/> |CMapiObjects:: fazer logoff  <br/> |MFCMAPI usa o método **IMAPISession:: logoff** para fazer logoff da sessão antes de liberá-lo.  <br/> |
   
> [!NOTE]
> Devido ao comportamento de desligamento rápido introduzido no Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010 e Microsoft Outlook 2013, os clientes nunca devem passar o parâmetro **MAPI_LOGOFF_SHARED** para [IMAPISession:: logoff](imapisession-logoff.md). Passar **MAPI_LOGOFF_SHARED** fará com que todos os clientes MAPI iniciem o desligamento e o comportamento inesperado ocorrerá. 
  
## <a name="see-also"></a>Confira também



[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Finalizar uma sessão MAPI](ending-a-mapi-session.md)

