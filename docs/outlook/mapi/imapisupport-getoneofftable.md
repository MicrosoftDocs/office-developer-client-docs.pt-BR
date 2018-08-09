---
title: IMAPISupportGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 51cd838164e3de28ab33d6ab8a08a021360f3183
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767229"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**Aplica-se a**: Outlook 
  
Retorna um ponteiro para a tabela MAPI único (uma lista de modelos que todos no catálogo de endereços provedores de suporte para a criação de novos destinatários).
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo das colunas de cadeia de caracteres. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As colunas de cadeia de caracteres estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela único.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A tabela único foi recuperada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::GetOneOffTable** é implementado para objetos de suporte do provedor de catálogo de endereços. Provedores de catálogo de endereço chamarem **GetOneOffTable** para recuperar a lista completa de modelos para a criação de novos destinatários. Esta tabela inclui modelos que oferecem suporte a provedores de catálogo de endereços que estão ativos na sessão, bem como modelos que ofereça suporte a MAPI. 
  
Os destinatários recém-criado podem ser usados para endereçar uma mensagem ou podem ser adicionados a um contêiner de catálogo de endereços.
  
Para obter uma lista das propriedades que compõem a coluna necessária definida nas tabelas únicas, consulte [Tabelas únicos](one-off-tables.md).
  
Definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ afeta o formato das colunas retornado dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) . Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornadas pelo método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se você estiver registrado para receber notificações de alterações para esta tabela único, você também receberá notificações de alterações nas tabelas de únicos dos outros provedores. Com base nessas notificações, você pode suportar novos tipos de endereço que são adicionados durante a sessão atual.
  
## <a name="see-also"></a>Confira também



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPISupport::NewEntry](imapisupport-newentry.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[Propriedade canônica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Tabelas únicas](one-off-tables.md)

