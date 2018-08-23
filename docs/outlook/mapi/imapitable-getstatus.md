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
ms.openlocfilehash: cda3de1719ec1b7cfca1a9ecdad7bc3b59a8b17d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571146"
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
  
> [out] Ponteiro para um valor que indica o status da tabela. Pode ser retornado um dos seguintes valores:
    
TBLSTAT_COMPLETE 
  
> Nenhuma operações estejam em andamento.
    
TBLSTAT_QCHANGED 
  
> O conteúdo da tabela expectantly foram alteradas. Esse valor de status não será retornado para que as alterações resultantes das operações de classificação ou restrição.
    
TBLSTAT_RESTRICT_ERROR 
  
> Ocorreu um erro durante uma operação [IMAPITable:: Restrict](imapitable-restrict.md) . 
    
TBLSTAT_RESTRICTING 
  
> Uma operação **IMAPITable:: Restrict** está em andamento. 
    
TBLSTAT_SETCOL_ERROR 
  
> Ocorreu um erro durante uma operação de [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
    
TBLSTAT_SETTING_COLS 
  
> Uma operação **IMAPITable::SetColumns** está em andamento. 
    
TBLSTAT_SORT_ERROR 
  
> Ocorreu um erro durante uma operação [IMAPITable:: SortTable](imapitable-sorttable.md) . 
    
TBLSTAT_SORTING 
  
> Uma operação **IMAPITable:: SortTable** está em andamento. 
    
 _lpulTableType_
  
> [out] Ponteiro para um valor que indica o tipo de tabela. Um dos seguintes tipos de três tabela pode ser retornado:
    
TBLTYPE_DYNAMIC 
  
> O conteúdo da tabela é dinâmico; as linhas e os valores de coluna podem alterar como as alterações de dados subjacente.
    
TBLTYPE_KEYSET 
  
> As linhas dentro da tabela são corrigidas, mas os valores das colunas dentro nessas linhas são dinâmicos e podem alterar como as alterações de dados subjacente.
    
TBLTYPE_SNAPSHOT 
  
> A tabela é estática e seu conteúdo não é alterados quando os dados subjacentes forem alterados.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Status da tabela foi retornado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPTable::GetStatus** recupera informações sobre o tipo e o status atual de uma tabela. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar **GetStatus** junto com três outros métodos **IMAPITable** para monitorar o status dessas operações e determinar o efeito sobre a tabela. Chame **GetStatus** depois de fazer uma das seguintes chamadas **IMAPITable** : 
  
- [IMAPITable:: Restrict](imapitable-restrict.md) para definir uma restrição. 
    
- [IMAPITable:: SortTable](imapitable-sorttable.md) para estabelecer uma ordem de classificação. 
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md) para definir um conjunto de coluna. 
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::GetStatus  <br/> |MFCMAPI usa o método **IMAPITable::GetStatus** para informar o status de uma tabela.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

