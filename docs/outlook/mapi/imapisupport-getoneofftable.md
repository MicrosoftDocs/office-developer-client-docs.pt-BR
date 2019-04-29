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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c0beec8a0b234794d3f623c4ceac773db698dd79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412755"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um ponteiro para a tabela única de MAPI (uma lista de modelos que todos os provedores de catálogo de endereços dão suporte à criação de novos destinatários).
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o tipo das colunas de cadeia de caracteres. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As colunas de cadeia de caracteres estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as colunas da cadeia de caracteres estarão no formato ANSI.
    
 _lppTable_
  
> bota Um ponteiro para um ponteiro para a tabela única.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela única foi recuperada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: GetOneOffTable** é implementado para objetos de suporte do provedor de catálogo de endereços. Os provedores de catálogo de endereços chamam **GetOneOffTable** para recuperar a lista completa de modelos para a criação de novos destinatários. Esta tabela inclui modelos que os provedores de catálogo de endereços estão ativos no suporte de sessão, bem como os modelos suportados por MAPI. 
  
Os destinatários recém-criados podem ser usados para endereçar uma mensagem ou podem ser adicionados a um contêiner de catálogo de endereços.
  
Para obter uma lista das propriedades que compõem o conjunto de colunas obrigatórios em tabelas únicas, consulte [one-off Tables](one-off-tables.md).
  
Definir o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ afeta o formato das colunas retornadas dos métodos IMAPITable [:: QueryColumns](imapitable-querycolumns.md) e IMAPITable [:: QueryRows](imapitable-queryrows.md) . Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornada pelo método imApitable [:: QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se você estiver registrado para receber notificações de alterações para esta tabela única, você também receberá notificações de alterações para as tabelas únicas de outros provedores. Com base nessas notificações, você pode dar suporte a novos tipos de endereço que são adicionados durante a sessão atual.
  
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

