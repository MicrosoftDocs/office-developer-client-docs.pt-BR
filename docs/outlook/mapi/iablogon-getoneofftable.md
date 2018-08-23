---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3732d8cbfaf9a6a10c62eae9e7a12b04de8a80ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583677"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma tabela de modelos únicos para a criação de destinatários a ser adicionado à lista de destinatários de uma mensagem de saída.
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo das colunas de cadeia de caracteres incluídos na tabela. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As colunas de cadeia de caracteres estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela único.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A tabela único foi recuperada com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e o provedor de catálogo de endereços não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e o provedor de catálogo de endereços suporta somente Unicode.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de catálogo de endereços não fornecer quaisquer modelos únicos.
    
## <a name="remarks"></a>Comentários

MAPI chama o método **GetOneOffTable** para tornar modelos únicos disponíveis para criar os destinatários. Os destinatários novos são adicionados à lista de destinatários de uma mensagem de saída. Provedores de catálogo de endereços devem oferecer suporte a notificação em seu tabela único para informar MAPI de modificações em modelos. MAPI mantém a tabela único abertas para habilitar a atualização dinâmica. 
  
Provedores de catálogo de endereços também podem oferecer suporte uma tabela único para cada um dos seus contêineres. Os chamadores recuperar esta tabela único chamando o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner e solicitar a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Os modelos disponíveis por meio de nesta tabela são usados para adicionar destinatários ao contêiner. Para uma discussão das diferenças entre os dois tipos de tabelas únicos, consulte [Implementando únicos Tables](implementing-one-off-tables.md).
  
Para obter uma lista das colunas na tabela de um provedor catálogo de endereços únicos necessárias, consulte [Tabelas únicos](one-off-tables.md).
  
## <a name="see-also"></a>Confira também



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

