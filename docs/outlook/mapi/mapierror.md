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
ms.openlocfilehash: 682e75c4e0a2f60dbd46a13b0b737ca4a8e18f3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409143"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  
> Número da versão da estrutura. O **membro ulVersion** é usado para expansão futura e deve ser definido como MAPI_ERROR_VERSION, atualmente definido como zero. 
    
 **lpszError**
  
> Ponteiro para uma cadeia de caracteres que descreve o erro. Essa cadeia de caracteres estará no formato Unicode se o  _parâmetro ulFlags_ para o método no qual essa estrutura é usada estiver definido como MAPI_UNICODE. 
    
 **lpszComponent**
  
> Ponteiro para uma cadeia de caracteres que descreve o componente que gerou o erro. Essa cadeia de caracteres estará no formato Unicode se o  _parâmetro ulFlags_ para o método no qual essa estrutura é usada estiver definido como MAPI_UNICODE. 
    
 **ulLowLevelError**
  
> Valor de erro de baixo nível que é usado somente quando o erro a ser retornado é de baixo nível.
    
 **ulContext**
  
> Valor que representa o local no componente apontado pelo membro **lpszComponent** que identifica onde ocorreu o erro. 
    
## <a name="remarks"></a>Comentários

A **estrutura MAPIERROR** é usada para descrever informações de erro. Os clientes e provedores de serviços passam um ponteiro para uma estrutura **MAPIERROR** no parâmetro _lppMAPIError_ do método [IMAPIProp::GetLastError.](imapiprop-getlasterror.md) **GetLastError** retorna informações sobre o erro anterior que ocorreu em um objeto. Os chamadores de **GetLastError** liberam a memória para a **estrutura MAPIERROR** chamando [MAPIFreeBuffer](mapifreebuffer.md).
  
O **membro lpszComponent** pode ser usado para mapear o arquivo de Ajuda do componente, se houver um. Os provedores de serviços devem limitar o tamanho da cadeia de caracteres do componente a 30 caracteres para que ela possa ser facilmente exibida em uma caixa de diálogo. O **membro ulContext** também pode ser usado para se referir a um tópico da Ajuda online em busca de erros comuns. 
  
Como os provedores de serviços não são obrigados a fornecer informações de erro detalhadas, os clientes não devem esperar nenhum dos membros da estrutura **MAPIERROR** que são retornados para conter dados válidos. No entanto, no mínimo MAPI recomenda que os provedores especifiquem informações nos membros **lpszComponent** e **ulContext.** 
  
Para obter mais informações sobre o tratamento de erros no MAPI, consulte [Tratamento de erros.](error-handling-in-mapi.md)
  
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

