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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 326a78ed512ec82a9f16b1540aad60954ab2d864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411873"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma tabela de modelos one-off para a criação de destinatários a serem adicionados à lista de destinatários de uma mensagem de saída.
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla o tipo de colunas de cadeia de caracteres incluídas na tabela. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As colunas de cadeia de caracteres estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela um-off.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela única foi recuperada com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE de endereços foi definido e o provedor de agendas não oferece suporte a Unicode ou MAPI_UNICODE não foi definido e o provedor de livro de endereços oferece suporte apenas a Unicode.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de agendas não fornece modelos one-off.
    
## <a name="remarks"></a>Comentários

O MAPI chama **o método GetOneOffTable** para disponibilizar modelos one-off para criar destinatários. Os novos destinatários são adicionados à lista de destinatários de uma mensagem de saída. Os provedores de agenda devem dar suporte à notificação em sua tabela única para informar o MAPI sobre modificações de modelo. O MAPI mantém a tabela única aberta para habilitar a atualização dinâmica. 
  
Os provedores de agendas também podem dar suporte a uma tabela única para cada um de seus contêineres. Os chamadores recuperam essa tabela única chamando o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner e solicitando a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Os modelos disponíveis por meio desta tabela são usados para adicionar destinatários ao contêiner. Para uma discussão sobre as diferenças entre os dois tipos de tabelas um-off, consulte Implementando One-Off [tabelas](implementing-one-off-tables.md).
  
Para uma lista das colunas necessárias na tabela única de um provedor de agendas, consulte [Tabelas One-Off.](one-off-tables.md)
  
## <a name="see-also"></a>Confira também



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

