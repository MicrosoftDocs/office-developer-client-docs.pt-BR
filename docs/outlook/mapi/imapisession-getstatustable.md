---
title: IMAPISessionGetStatusTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 17e936093536f548d16021523d9434f09777c6d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407134"
---
# <a name="imapisessiongetstatustable"></a>IMAPISession::GetStatusTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à tabela de status, uma tabela que contém informações sobre todos os recursos MAPI na sessão.
  
```cpp
HRESULT GetStatusTable(
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
  
> [out] Um ponteiro para um ponteiro para a tabela de status.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPISession::GetStatusTable** fornece acesso à tabela de status que contém informações sobre todos os recursos MAPI na sessão. Há uma linha na tabela para obter informações sobre o subsistema MAPI, uma linha para o spooler MAPI, uma linha para o livro de endereços integrado e uma linha para cada provedor de serviços no perfil. 
  
Para uma lista completa das colunas necessárias e opcionais na tabela de status, consulte [Tabelas de Status.](status-tables.md) 
  
A definição MAPI_UNICODE sinalizador de texto no parâmetro _ulFlags_ afeta o formato das colunas retornadas dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md) Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornada pelo método [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnStatusTable  <br/> |MFCMAPI usa o **método IMAPISession::GetStatusTable** para obter a tabela de status a ser renderizada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Tabelas de Status](status-tables.md)

