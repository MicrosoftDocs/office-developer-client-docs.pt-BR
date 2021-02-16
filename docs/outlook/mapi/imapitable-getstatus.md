---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ec305fc872d1bf1718592dabdd230617d50d3f54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434330"
---
# <a name="imapitablegetstatus"></a>IMAPITable::GetStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o status e o tipo da tabela.
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a>Parâmetros

 _lpulTableStatus_
  
> [out] Ponteiro para um valor que indica o status da tabela. Um dos seguintes valores pode ser retornado:
    
TBLSTAT_COMPLETE 
  
> Nenhuma operação está em andamento.
    
TBLSTAT_QCHANGED 
  
> O conteúdo da tabela foi alterado de forma esperada. Esse valor de status não é retornado para alterações resultantes de operações de classificação ou restrição.
    
TBLSTAT_RESTRICT_ERROR 
  
> Ocorreu um erro durante uma [operação IMAPITable::Restrict.](imapitable-restrict.md) 
    
TBLSTAT_RESTRICTING 
  
> Uma **operação IMAPITable::Restrict** está em andamento. 
    
TBLSTAT_SETCOL_ERROR 
  
> Ocorreu um erro durante uma [operação IMAPITable::SetColumns.](imapitable-setcolumns.md) 
    
TBLSTAT_SETTING_COLS 
  
> Uma **operação IMAPITable::SetColumns** está em andamento. 
    
TBLSTAT_SORT_ERROR 
  
> Ocorreu um erro durante uma [operação IMAPITable::SortTable.](imapitable-sorttable.md) 
    
TBLSTAT_SORTING 
  
> Uma **operação IMAPITable::SortTable** está em andamento. 
    
 _lpulTableType_
  
> [out] Ponteiro para um valor que indica o tipo da tabela. Um dos três tipos de tabela a seguir pode ser retornado:
    
TBLTYPE_DYNAMIC 
  
> O conteúdo do índice é dinâmico; as linhas e os valores de coluna podem mudar à medida que os dados subjacentes mudam.
    
TBLTYPE_KEYSET 
  
> As linhas dentro da tabela são fixas, mas os valores das colunas dentro dessas linhas são dinâmicos e podem mudar à medida que os dados subjacentes mudam.
    
TBLTYPE_SNAPSHOT 
  
> A tabela é estática e seu conteúdo não muda quando os dados subjacentes mudam.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O status da tabela foi retornado com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPTable::GetStatus** recupera informações sobre o tipo e o status atual de uma tabela. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar **GetStatus** em conjunto com três outros métodos **IMAPITable** para monitorar o status dessas operações e determinar o efeito na tabela. Chame **GetStatus** depois de fazer uma das seguintes **chamadas IMAPITable:** 
  
- [IMAPITable::Restrict](imapitable-restrict.md) para definir uma restrição. 
    
- [IMAPITable::SortTable](imapitable-sorttable.md) para estabelecer uma ordem de classificação. 
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md) para definir um conjunto de colunas. 
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::GetStatus  <br/> |MFCMAPI usa o **método IMAPITable::GetStatus** para relatar o status de uma tabela.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

