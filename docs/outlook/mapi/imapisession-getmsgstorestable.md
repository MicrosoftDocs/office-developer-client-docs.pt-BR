---
title: IMAPISessionGetMsgStoresTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5fced633023ebf00efaf5b667dc7994eeb5de316
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428134"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à tabela do armazenamento de mensagens que contém informações sobre todos os armazenamentos de mensagens no perfil de sessão.
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que determina o formato para colunas que são cadeias de caracteres. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As colunas de cadeia de caracteres estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela do armazenamento de mensagens.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela foi retornada com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> O MAPI_UNICODE sinalizador foi definido e a sessão não dá suporte a Unicode.
    
## <a name="remarks"></a>Comentários

O método **IMAPISession::GetMsgStoresTable** recupera um ponteiro para a tabela de armazenamento de mensagens, uma tabela mantida por MAPI que contém informações sobre cada armazenamento de mensagens abertas no perfil. 
  
Para uma lista completa das colunas necessárias e opcionais na tabela do armazenamento de mensagens, consulte [Tabelas do Armazenamento de Mensagens.](message-store-tables.md) 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Como o MAPI atualiza a tabela do armazenamento de mensagens durante a sessão sempre que ocorrem alterações, chame o método **Advise** da tabela de armazenamento de mensagens para registrar para ser notificado dessas alterações. As alterações possíveis incluem a adição de novos armazenamentos de mensagens, remoção de armazenamentos existentes e alterações no armazenamento padrão. 
  
A definição MAPI_UNICODE sinalizador de texto no parâmetro _ulFlags_ afeta o formato das colunas retornadas dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md) Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornada pelo método [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenMessageStoreTable  <br/> |MFCMAPI usa o método **IMAPISession::GetMsgStoresTable** para obter a tabela de armazenamento de mensagens para que ela possa ser renderizada na caixa de diálogo principal de MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Tabelas do Armazenamento de Mensagens](message-store-tables.md)

