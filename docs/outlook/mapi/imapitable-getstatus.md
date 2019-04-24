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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328893"
---
# <a name="imapitablegetstatus"></a>IMAPITable::GetStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o tipo e o status da tabela.
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a>Parâmetros

 _lpulTableStatus_
  
> bota Ponteiro para um valor que indica o status da tabela. Um dos valores a seguir pode ser retornado:
    
TBLSTAT_COMPLETE 
  
> Nenhuma operação está em andamento.
    
TBLSTAT_QCHANGED 
  
> O conteúdo da tabela tem expectantly alterado. Esse valor de status não é retornado para alterações resultantes de operações de classificação ou restrição.
    
TBLSTAT_RESTRICT_ERROR 
  
> Ocorreu um erro durante uma operação imApitable [:: Restrict](imapitable-restrict.md) . 
    
TBLSTAT_RESTRICTING 
  
> Uma operação imApitable **:: Restrict** está em andamento. 
    
TBLSTAT_SETCOL_ERROR 
  
> Ocorreu um erro durante uma operação imApitable [::](imapitable-setcolumns.md) SetColumns. 
    
TBLSTAT_SETTING_COLS 
  
> Uma operação imApitable **::** SetColumns está em andamento. 
    
TBLSTAT_SORT_ERROR 
  
> Ocorreu um erro durante uma operação imApitable [:: SortTable](imapitable-sorttable.md) . 
    
TBLSTAT_SORTING 
  
> Uma operação imApitable **:: SortTable** está em andamento. 
    
 _lpulTableType_
  
> bota Ponteiro para um valor que indica o tipo da tabela. Um dos três tipos de tabela a seguir pode ser retornado:
    
TBLTYPE_DYNAMIC 
  
> O conteúdo da tabela é dinâmico; os valores de linhas e colunas podem ser alterados à medida que os dados subjacentes são alterados.
    
TBLTYPE_KEYSET 
  
> As linhas dentro da tabela são corrigidas, mas os valores das colunas dentro dessas linhas são dinâmicos e podem ser alterados à medida que os dados subjacentes são alterados.
    
TBLTYPE_SNAPSHOT 
  
> A tabela é estática, e seu conteúdo não é alterado quando os dados subjacentes são alterados.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O status da tabela foi retornado com êxito.
    
## <a name="remarks"></a>Comentários

O método **imaptable:: GetStatus** recupera informações sobre o tipo de tabela e o status atual. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar **GetStatus** em conjunto com três outros **** métodos IMAPITable para monitorar o status dessas operações e determinar o efeito sobre a tabela. Chame **GetStatus** após fazer uma das seguintes chamadas **** IMAPITable: 
  
- [IMAPITable:: strict](imapitable-restrict.md) para definir uma restrição. 
    
- [IMAPITable:: SortTable](imapitable-sorttable.md) para estabelecer uma ordem de classificação. 
    
- [IMAPITable::](imapitable-setcolumns.md) SetColumns para definir um conjunto de colunas. 
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl:: GetStatus  <br/> |MFCMAPI usa o método imApitable **:: GetStatus** para relatar o status de uma tabela.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

