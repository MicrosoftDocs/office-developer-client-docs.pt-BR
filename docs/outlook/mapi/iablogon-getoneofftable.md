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
  
Retorna uma tabela de modelos únicos para a criação de destinatários a serem adicionados à lista de destinatários de uma mensagem de saída.
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o tipo de colunas de cadeia de caracteres incluído na tabela. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As colunas de cadeia de caracteres estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as colunas da cadeia de caracteres estarão no formato ANSI.
    
 _lppTable_
  
> bota Um ponteiro para um ponteiro para a tabela única.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela única foi recuperada com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e o provedor de catálogo de endereços não é compatível com Unicode, ou o MAPI_UNICODE não foi definido e o provedor de catálogo de endereços oferece suporte somente a Unicode.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de catálogo de endereços não fornece modelos únicos.
    
## <a name="remarks"></a>Comentários

O MAPI chama o método **GetOneOffTable** para tornar os modelos one-off disponíveis para criar destinatários. Os novos destinatários são adicionados à lista de destinatários de uma mensagem de saída. Os provedores de catálogo de endereços devem dar suporte à notificação em sua tabela única para informar a MAPI de modificações de modelo. O MAPI mantém a tabela única aberta para habilitar a atualização dinâmica. 
  
Os provedores de catálogos de endereços também podem oferecer suporte a uma tabela única para cada um de seus contêineres. Os chamadores recuperam essa tabela única chamando o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do contêiner e solicitando a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Os modelos disponíveis nesta tabela são usados para adicionar destinatários ao contêiner. Para obter uma discussão sobre as diferenças entre os dois tipos de tabelas individuais, consulte [implementIng one-off Tables](implementing-one-off-tables.md).
  
Para obter uma lista das colunas obrigatórias em uma tabela de um provedor de catálogo de endereços, consulte [one-off Tables](one-off-tables.md).
  
## <a name="see-also"></a>Confira também



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

