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
ms.openlocfilehash: 303c2ef855d5cfc1d6614bda92b46c2da97717c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421351"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à tabela de pastas de recebimento, uma tabela que inclui informações sobre todas as pastas de recebimento do repositório de mensagens.
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam O acesso à tabela. Os seguintes sinalizadores podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que o **GetReceiveFolderTable** seja retornado com êxito, possivelmente antes de a tabela ficar totalmente disponível para o chamador. Se a tabela não estiver totalmente disponível, fazer uma chamada de tabela subsequente poderá gerar um erro. 
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
 _lppTable_
  
> bota Um ponteiro para um ponteiro para a tabela de pastas de recebimento.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela de pastas de recebimento foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore:: GetReceiveFolderTable** fornece acesso a uma tabela que mostra as configurações de propriedade de todas as pastas de recebimento do repositório de mensagens. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Para obter uma lista de colunas obrigatórias em uma tabela de pastas de recebimento, consulte [Receive Folder Tables](receive-folder-tables.md). 
  
Implemente suas tabelas de pastas de recebimento para suportar a definição de restrições de propriedade na propriedade **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Isso permite o acesso fácil a pastas de recebimento específicas.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Definir o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ afeta o formato das colunas retornadas dos métodos IMAPITable [:: QueryColumns](imapitable-querycolumns.md) e IMAPITable [:: QueryRows](imapitable-queryrows.md) . Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornada pelo método imApitable [:: QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnDisplayReceiveFolderTable  <br/> |MFCMAPI usa o método **IMsgStore:: GetReceiveFolderTable** para obter a exibição da tabela de pastas de recebimento.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

