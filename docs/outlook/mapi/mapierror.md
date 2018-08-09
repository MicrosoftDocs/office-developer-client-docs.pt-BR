---
title: MAPIERROR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIERROR
api_type:
- COM
ms.assetid: e04c2228-aa0a-4958-b5b2-6467e93ab613
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d0ddff638e26940ea74932a8a491455f67cc8dd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767981"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**Aplica-se a**: Outlook 
  
Fornece informações detalhadas sobre um erro, normalmente gerado pelo sistema operacional, MAPI ou um provedor de serviços. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _MAPIERROR
{
  ULONG ulVersion;
  LPSTR lpszError;
  LPSTR lpszComponent;
  ULONG ulLowLevelError;
  ULONG ulContext;
} MAPIERROR, FAR * LPMAPIERROR;

```

## <a name="members"></a>Members

 **ulVersion**
  
> Número de versão da estrutura. O membro **ulVersion** é usado para expansão futura e deve ser definido como MAPI_ERROR_VERSION, que atualmente é definido como zero. 
    
 **lpszError**
  
> Ponteiro para uma cadeia de caracteres que descreve o erro. Esta cadeia de caracteres estará no formato Unicode, se o parâmetro _ulFlags_ para o método no qual esta estrutura é usada estiver definido como MAPI_UNICODE. 
    
 **lpszComponent**
  
> Ponteiro para uma cadeia de caracteres que descreve o componente que gerou o erro. Esta cadeia de caracteres estará no formato Unicode, se o parâmetro _ulFlags_ para o método no qual esta estrutura é usada estiver definido como MAPI_UNICODE. 
    
 **ulLowLevelError**
  
> Valor de erro de baixo nível que é usado somente quando o erro a ser retornado é baixo nível.
    
 **ulContext**
  
> O valor que representa o local no componente apontado pelo membro **lpszComponent** que identifica onde ocorreu o erro. 
    
## <a name="remarks"></a>Comentários

A estrutura **MAPIERROR** é usada para descrever as informações de erro. Provedores de serviços e clientes passam um ponteiro para uma estrutura **MAPIERROR** no parâmetro _lppMAPIError_ do método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) . **GetLastError** retorna informações sobre o erro anterior que ocorreu a um objeto. Os chamadores da **GetLastError** liberar a memória para a estrutura **MAPIERROR** chamando [MAPIFreeBuffer](mapifreebuffer.md).
  
O membro **lpszComponent** pode ser usado para mapear o arquivo de Ajuda do componente, se houver uma. Provedores de serviços devem limitar o tamanho da cadeia de caracteres de componente para 30 caracteres para que ela possa ser facilmente exibida em uma caixa de diálogo. O membro **ulContext** também pode ser usado para se referir a um tópico da Ajuda online para erros comuns. 
  
Como provedores de serviços não são necessários para fornecer informações de erro detalhadas, os clientes não devem esperar que qualquer um dos membros da estrutura **MAPIERROR** que são retornados para conter dados válidos. No entanto, em um mínimo MAPI recomenda que provedores especificam informações nos membros **lpszComponent** e **ulContext** . 
  
Para obter mais informações sobre o tratamento de erros no MAPI, consulte o [Tratamento de erros](error-handling-in-mapi.md).
  
## <a name="see-also"></a>Confira também



[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IABProvider::Logon](iabprovider-logon.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md)
  
[IMSLogon::GetLastError](imslogon-getlasterror.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[IProfAdmin::GetLastError](iprofadmin-getlasterror.md)
  
[IProviderAdmin::GetLastError](iprovideradmin-getlasterror.md)


[Estruturas MAPI](mapi-structures.md)

