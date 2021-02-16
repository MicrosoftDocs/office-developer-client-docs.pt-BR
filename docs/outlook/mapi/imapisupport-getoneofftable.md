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
  
Retorna um ponteiro para a tabela única MAPI (uma lista de modelos que todos os provedores de agenda de endereços suportam para criar novos destinatários).
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o tipo das colunas de cadeia de caracteres. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As colunas de cadeia de caracteres estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela um-off.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela única foi recuperada com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::GetOneOffTable** é implementado para objetos de suporte do provedor de agendas de endereços. Os provedores de agendamento de endereço chamam **GetOneOffTable** para recuperar a lista completa de modelos para criar novos destinatários. Esta tabela inclui modelos que abordam provedores de livro de endereços que estão ativos no suporte à sessão, bem como modelos compatíveis com MAPI. 
  
Os destinatários recém-criados podem ser usados para lidar com uma mensagem ou podem ser adicionados a um contêiner de um livro de endereços.
  
Para uma lista das propriedades que com o conjunto de colunas necessários em tabelas únicas, consulte [Tabelas Únicas.](one-off-tables.md)
  
A definição MAPI_UNICODE sinalizador de texto no parâmetro _ulFlags_ afeta o formato das colunas retornadas dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md) Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornada pelo método [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se você estiver registrado para receber notificações de alterações nesta tabela única, também receberá notificações de alterações nas tabelas one-off de outros provedores. Com base nessas notificações, você pode dar suporte a novos tipos de endereços adicionados durante a sessão atual.
  
## <a name="see-also"></a>Confira também



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPISupport::NewEntry](imapisupport-newentry.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[Propriedade canônica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Tabelas One-Off](one-off-tables.md)

