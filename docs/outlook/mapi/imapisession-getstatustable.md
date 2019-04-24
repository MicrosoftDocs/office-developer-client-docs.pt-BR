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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338756"
---
# <a name="imapisessiongetstatustable"></a>IMAPISession::GetStatusTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à tabela status, uma tabela que contém informações sobre todos os recursos MAPI na sessão.
  
```cpp
HRESULT GetStatusTable(
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
  
> bota Um ponteiro para um ponteiro para a tabela de status.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela foi retornada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISession::** getstatustable fornece acesso à tabela de status que contém informações sobre todos os recursos MAPI na sessão. Há uma linha na tabela para obter informações sobre o subsistema MAPI, uma linha para o spooler MAPI, uma linha para o catálogo de endereços integrado e uma linha para cada provedor de serviços no perfil. 
  
Para obter uma lista completa de colunas obrigatórias e opcionais na tabela status, consulte [tabelas de status](status-tables.md). 
  
Definir o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ afeta o formato das colunas retornadas dos métodos IMAPITable [:: QueryColumns](imapitable-querycolumns.md) e IMAPITable [:: QueryRows](imapitable-queryrows.md) . Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornada pelo método imApitable [:: QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: onStatustable  <br/> |MFCMAPI usa o método **IMAPISession::** getstatustable para obter a tabela de status a ser renderizada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Tabelas de status](status-tables.md)

