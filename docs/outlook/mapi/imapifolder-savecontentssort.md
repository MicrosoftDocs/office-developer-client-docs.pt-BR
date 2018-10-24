---
title: IMAPIFolderSaveContentsSort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SaveContentsSort
api_type:
- COM
ms.assetid: 5ae3fdf0-6193-4c1f-bd2e-d69c56d69773
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1f79265c4356747e64aa8102dd4486db229baf5a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579659"
---
# <a name="imapifoldersavecontentssort"></a>IMAPIFolder::SaveContentsSort

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define a ordem de classificação padrão para a tabela de conteúdo de uma pasta.
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpSortCriteria_
  
> [in] Um ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) que contém a ordem de classificação padrão. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a ordem de classificação padrão é definida. O seguinte sinalizador pode ser definido:
    
RECURSIVE_SORT 
  
> O conjunto de ordem de classificação padrão se aplica à pasta indicada e todas as suas subpastas.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A ordem de classificação for salva com êxito.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de armazenamento de mensagem não suporta a salvando uma ordem de classificação para suas tabelas de conteúdo de pasta.
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder::SaveContentsSort** estabelece uma ordem de classificação padrão para a tabela de conteúdo de uma pasta. Ou seja, quando um cliente chama o método de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) da pasta após o código chama **SaveContentsSort**, as linhas da tabela de conteúdo retornado aparecerá na ordem estabelecida pelo **SaveContentsSort**.
  
Nem todos os provedores de armazenamento de mensagem suportam **SaveContentsSort**; é aceitável para provedores de armazenamento de mensagem retornar MAPI_E_NO_SUPPORT do método **SaveContentsSort** . 
  
## <a name="see-also"></a>Confira também



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

