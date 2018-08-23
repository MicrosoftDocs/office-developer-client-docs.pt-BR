---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 681fd68fc068633912df1cb7f060b8c4111b5de8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566534"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à tabela de pasta de recebimento, uma tabela que inclui informações sobre todas as pastas de recebimento para o armazenamento de mensagens.
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controles tabela acesso. Sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **GetReceiveFolderTable** retornar com êxito, possivelmente antes que a tabela é totalmente disponível para o chamador. Se a tabela não estiver totalmente disponível, fazendo uma chamada de tabela subsequentes pode gerar um erro. 
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela de pasta de recebimento.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A tabela de pasta de recebimento foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore::GetReceiveFolderTable** fornece acesso a uma tabela que mostra que as configurações de propriedade para o armazenamento de mensagens todos recebem pastas. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Para obter uma lista das colunas obrigatórias em uma tabela de pasta de recebimento, consulte as [Tabelas de pasta de recebimento](receive-folder-tables.md). 
  
Implementar sua receber tabelas de pasta para oferecer suporte a restrições de propriedades de configuração na propriedade **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Este permite o acesso fácil a determinado receber pastas.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ afeta o formato das colunas retornado dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) . Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornadas pelo método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDisplayReceiveFolderTable  <br/> |MFCMAPI usa o método **IMsgStore::GetReceiveFolderTable** para obter a tabela de pasta de recebimento para exibir.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

