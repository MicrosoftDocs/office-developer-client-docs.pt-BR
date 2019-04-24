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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338826"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à tabela do repositório de mensagens que contém informações sobre todos os repositórios de mensagens no perfil da sessão.
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que determina o formato das colunas que são cadeias de caracteres. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As colunas de cadeia de caracteres estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as colunas da cadeia de caracteres estarão no formato ANSI.
    
 _lppTable_
  
> bota Um ponteiro para um ponteiro para a tabela do repositório de mensagens.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela foi retornada com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a sessão não dá suporte a Unicode.
    
## <a name="remarks"></a>Comentários

O método **IMAPISession:: GetMsgStoresTable** recupera um ponteiro para a tabela do repositório de mensagens, uma tabela mantida por MAPI que contém informações sobre cada repositório de mensagens aberto no perfil. 
  
Para obter uma lista completa de colunas obrigatórias e opcionais na tabela do repositório de mensagens, consulte [Message Store Tables](message-store-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Como o MAPI atualiza a tabela do repositório de mensagens durante a sessão sempre que ocorrerem alterações, chame o método **Advise** da tabela do repositório de mensagens a ser registrado para ser notificado dessas alterações. As alterações possíveis incluem a adição de novos repositórios de mensagens, remoção de repositórios existentes e alterações no repositório padrão. 
  
Definir o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ afeta o formato das colunas retornadas dos métodos IMAPITable [:: QueryColumns](imapitable-querycolumns.md) e IMAPITable [:: QueryRows](imapitable-queryrows.md) . Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornada pelo método imApitable [:: QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnOpenMessageStoreTable  <br/> |MFCMAPI usa o método **IMAPISession:: GetMsgStoresTable** para obter a tabela do repositório de mensagens, de forma que ela possa ser renderizada na caixa de diálogo principal do MFCMAPI.  <br/> |
   
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
  
[Tabelas de repositório de mensagens](message-store-tables.md)

