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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: ba540b0fd3371b3e12be9eeeb102a9bd9d7e8d22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767168"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**Aplica-se a**: Outlook 
  
Fornece acesso à tabela do repositório de mensagem que contém informações sobre todos os repositórios de mensagem no perfil da sessão.
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que determina o formato de colunas que são cadeias de caracteres. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As colunas de cadeia de caracteres estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela de repositório de mensagens.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A tabela foi retornada com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a sessão não dá suporte a Unicode.
    
## <a name="remarks"></a>Coment�rios

O método **IMAPISession::GetMsgStoresTable** recupera um ponteiro para a tabela de repositório de mensagens, uma tabela mantidas por MAPI que contém informações sobre cada repositório de mensagem aberta no perfil. 
  
Para obter uma lista completa das colunas obrigatórios e opcionais na mensagem repositório tabela, consulte [Tabelas de armazenar mensagens](message-store-tables.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Como MAPI atualiza a tabela de repositório de mensagens durante a sessão sempre que ocorrerem alterações, chame o método **Advise** a tabela de repositório de mensagens para registrar para ser notificado sobre essas alterações. Alterações possíveis incluem a adição de novas lojas de mensagem, remoção de existentes armazena e altera para o repositório padrão. 
  
Definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ afeta o formato das colunas retornado dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) . Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornadas pelo método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenMessageStoreTable  <br/> |MFCMAPI usa o método **IMAPISession::GetMsgStoresTable** para obter a tabela de repositório de mensagens, de modo que ele poderá ser renderizado da caixa de diálogo principal do MFCMAPI.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable:: QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable:: SortTable](imapitable-sorttable.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Tabelas de armazenamento de mensagens](message-store-tables.md)

